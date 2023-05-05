# Lab 10 #
### For Lab 10, I learned about Blockchain ###
### I started with the commands on hash_value.py and received the following (Note: I use command python not python3): ###
```
C:\Users\cesar\OneDrive - stevens.edu\Spring 2023 (3rd Year)\EE-322 D6\iot\lesson10>cat hash_value.py
"""
https://docs.python.org/3/using/cmdline.html#envvar-PYTHONHASHSEED
If PYTHONHASHSEED is not set or set to random, a random value is used to to seed the hashes of str and bytes objects.
If PYTHONHASHSEED is set to an integer value, it is used as a fixed seed for generating the hash() of the types covered by the hash randomization.
Its purpose is to allow repeatable hashing, such as for selftests for the interpreter itself, or to allow a cluster of python processes to share hash values.
The integer must be a decimal number in the range [0,4294967295]. Specifying the value 0 will disable hash randomization.

https://www.programiz.com/python-programming/methods/built-in/hash
hash(object) returns the hash value of the object (if it has one). Hash values are integers.
They are used to quickly compare dictionary keys during a dictionary lookup.
Numeric values that compare equal have the same hash value even if they are of different types, as is the case for 1 and 1.0.
For objects with custom __hash__() methods, note that hash() truncates the return value based on the bit width of the host machine.
"""

# hash for integer unchanged
print('The hash for 1 is:', hash(1))

# hash for decimal
print('The hash for 1.0 is:',hash(1.0))
print('The hash for 3.14 is:',hash(3.14))

# hash for string
print('The hash for Python is:', hash('Python'))

# hash for a tuple of vowels
vowels = ('a', 'e', 'i', 'o', 'u')
print('The hash for a tuple of vowels is:', hash(vowels))

# hash for a custom object
class Person:
    def __init__(self, age, name):
        self.age = age
        self.name = name
    def __eq__(self, other):
        return self.age == other.age and self.name == other.name
    def __hash__(self):
        return hash((self.age, self.name))
person = Person(23, 'Adam')
print('The hash for an object of person is:', hash(person))

C:\Users\cesar\OneDrive - stevens.edu\Spring 2023 (3rd Year)\EE-322 D6\iot\lesson10>python hash_value.py
The hash for 1 is: 1
The hash for 1.0 is: 1
The hash for 3.14 is: 322818021289917443
The hash for Python is: 3555978470055951170
The hash for a tuple of vowels is: 8581631274363806147
The hash for an object of person is: -7570254409193631345
```

### Next, I execute the following code in python within my terminal as follows: ###
```
C:\Users\cesar\OneDrive - stevens.edu\Spring 2023 (3rd Year)\EE-322 D6>python
Python 3.8.3 (tags/v3.8.3:6f8c832, May 13 2020, 22:37:02) [MSC v.1924 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import hashlib
>>> m = hashlib.sha256(b"hello, world")
>>> m.hexdigest()
'09ca7e4eaa6e8ae9c7d261167129184883644d07dfba7cbfbc4c8a2e08360d5b'
>>> m.digest_size
32
>>> m.block_size
64
>>> exit()
```
 ### I then build the tiniest blockchain in less than 50 lines of Python by Gerald Nash: ###
 ```
 C:\Users\cesar\OneDrive - stevens.edu\Spring 2023 (3rd Year)\EE-322 D6\iot\lesson10>cat snakecoin.py
# Gerald Nash, "Let's build the tiniest blockchain in less than 50 lines of Python"
import hashlib as hasher
import datetime as date

# Define what a Snakecoin block is
class Block:
  def __init__(self, index, timestamp, data, previous_hash):
    self.index = index
    self.timestamp = timestamp
    self.data = data
    self.previous_hash = previous_hash
    self.hash = self.hash_block()

  def hash_block(self):
    sha = hasher.sha256()
    sha.update(str(self.index).encode() + str(self.timestamp).encode() + str(self.data).encode() + str(self.previous_hash).encode())
    return sha.hexdigest()

# Generate genesis block
def create_genesis_block():
  # Manually construct a block with
  # index zero and arbitrary previous hash
  return Block(0, date.datetime.now(), "Genesis Block", "0")

# Generate all later blocks in the blockchain
def next_block(last_block):
  this_index = last_block.index + 1
  this_timestamp = date.datetime.now()
  this_data = "Hey! I'm block " + str(this_index)
  this_hash = last_block.hash
  return Block(this_index, this_timestamp, this_data, this_hash)

# Create the blockchain and add the genesis block
blockchain = [create_genesis_block()]
previous_block = blockchain[0]

# How many blocks should we add to the chain
# after the genesis block
num_of_blocks_to_add = 20

# Add blocks to the chain
for i in range(0, num_of_blocks_to_add):
  block_to_add = next_block(previous_block)
  blockchain.append(block_to_add)
  previous_block = block_to_add
  # Tell everyone about it!
  print("Block #{} has been added to the blockchain!".format(block_to_add.index))
  print("Hash: {}\n".format(block_to_add.hash))

C:\Users\cesar\OneDrive - stevens.edu\Spring 2023 (3rd Year)\EE-322 D6\iot\lesson10>python snakecoin.py
Block #1 has been added to the blockchain!
Hash: 51564d9cb7b3f70ec2b11e63e2f4f55c467ea8c857e070b33e8c3489e1117d0a

Block #2 has been added to the blockchain!
Hash: 95eb19f5118757b1d61f5c3a30f2b9ff803dcbcb1d7d4d54ac6ad12def29bdef

Block #3 has been added to the blockchain!
Hash: 966bd792a11ae255c678447865af113ca3dc523225e93218ea3b3b90cb5d140c

Block #4 has been added to the blockchain!
Hash: 32c6a658d2c4a2ee4e7440d3e6858339c4944379086b8d82e51b301e6c58e677

Block #5 has been added to the blockchain!
Hash: 2c3f75d71aaa312c6b4649124dc4374a6ab25a0aff4519c9682195e3e46ad151

Block #6 has been added to the blockchain!
Hash: 465a41b02c84b49df45cc2e0ae942df34f7a8afb569677b240429ecc23f183d8

Block #7 has been added to the blockchain!
Hash: 7d8f50222e4eaadd098ef82d1a17581c11f310bccfb6e902ee9590fe75299c40

Block #8 has been added to the blockchain!
Hash: 23436771239d512ecf39bb85b701fbd64988a9c12c8d62b97dabc69173155f9e

Block #9 has been added to the blockchain!
Hash: 2e2bc7898f227468cacc03ad2edda281391091ca63e6fb21886e096441166eb0

Block #10 has been added to the blockchain!
Hash: 184f8ac462306f68de755f4fb4cf333a8a946f73ab5150a07ae43ed2ef89aa20

Block #11 has been added to the blockchain!
Hash: 34ededdda52b65c84e778a189bc472fb893f2f3c0fc95beb5d874b928daf4179

Block #12 has been added to the blockchain!
Hash: 1d1174404512c9a00043448dd25019fb61ff7046df4fd4e35c3310fffb303735

Block #13 has been added to the blockchain!
Hash: 4bcc8214704e8791a10798b0aa5d766e923fef576eef15a0340fbbefe5642031

Block #14 has been added to the blockchain!
Hash: ddee870a03539f7df20a11f29a6c38d8a5ad67583649399b4c4bee7d2fe27d74

Block #15 has been added to the blockchain!
Hash: b95eaa126e1c79628fff73bfe53d2b8f69092a1ab080ea935f3b0d798e0f345b

Block #16 has been added to the blockchain!
Hash: cc6b475676314bc2898aa4d9451b9844a9dfe504088216b3d7f0990e9cd85a41

Block #17 has been added to the blockchain!
Hash: 91a3593ba33fd2821c69e140b50ee873ea798f8a2901e974d5ca4c69f05933bb

Block #18 has been added to the blockchain!
Hash: 0425fbb952c473e3372c22a3dff18f2d6e24d750fe5593ee8e0383bf21ef36c2

Block #19 has been added to the blockchain!
Hash: b72390dd4e3417b3a8bd934a42958cefccff33ec77dcaae8a4f569447fc02899

Block #20 has been added to the blockchain!
Hash: 3c0c461bc0be9ce562fa3c728b7e131b69d9234da2954e97cef8e44118d54acf
```

### I then open 2 terminals for the next part where I will be making the blockchain bigger ###
### In terminal 1, I executed the following: ###
```
C:\Users\cesar\OneDrive - stevens.edu\Spring 2023 (3rd Year)\EE-322 D6\iot\lesson10>cat snakecoin-server-full-code.py
# Gerald Nash, "Let’s Make the Tiniest Blockchain Bigger Part 2: With More Lines of Python"
# Referred to https://www.pythonanywhere.com/forums/topic/12382/ that fixed sha.update() TypeError: Unicode-objects must be encoded before hashing
# Running on http://127.0.0.1:5000/mine (Reload the page to mine and press CTRL+C to quit)
from flask import Flask
from flask import request
import json
import requests
import hashlib as hasher
import datetime as date
from flask import send_from_directory
import os
node = Flask(__name__)

# Define what a Snakecoin block is
class Block:
  def __init__(self, index, timestamp, data, previous_hash):
    self.index = index
    self.timestamp = timestamp
    self.data = data
    self.previous_hash = previous_hash
    self.hash = self.hash_block()

  def hash_block(self):
    sha = hasher.sha256()
#    sha.update(str(self.index) + str(self.timestamp) + str(self.data) + str(self.previous_hash))
    sha.update((str(self.index) + str(self.timestamp) + str(self.data) + str(self.previous_hash)).encode("utf-8"))
    return sha.hexdigest()

# Generate genesis block
def create_genesis_block():
  # Manually construct a block with
  # index zero and arbitrary previous hash
  return Block(0, date.datetime.now(), {
    "proof-of-work": 9,
    "transactions": None
  }, "0")

# A completely random address of the owner of this node
miner_address = "q3nf394hjg-random-miner-address-34nf3i4nflkn3oi"
# This node's blockchain copy
blockchain = []
blockchain.append(create_genesis_block())
# Store the transactions that
# this node has in a list
this_nodes_transactions = []
# Store the url data of every
# other node in the network
# so that we can communicate
# with them
peer_nodes = []
# A variable to deciding if we're mining or not
mining = True

@node.route("/")
def hello():
    return "SnakeCoin Server"

@node.route('/favicon.ico')
def favicon():
    return send_from_directory(os.path.join(node.root_path, 'static'),
                               'favicon.ico',
                               mimetype='image/vnd.microsoft.icon')

@node.route('/txion', methods=['POST'])
def transaction():
  # On each new POST request,
  # we extract the transaction data
  new_txion = request.get_json()
  # Then we add the transaction to our list
  this_nodes_transactions.append(new_txion)
  # Because the transaction was successfully
  # submitted, we log it to our console
  print("New transaction")
  print(("FROM: {}".format(new_txion['from'].encode('ascii','replace'))))
  print(("TO: {}".format(new_txion['to'].encode('ascii','replace'))))
  print(("AMOUNT: {}\n".format(new_txion['amount'])))
  # Then we let the client know it worked out
  return "Transaction submission successful\n"

@node.route('/blocks', methods=['GET'])
def get_blocks():
  chain_to_send = blockchain
  # Convert our blocks into dictionaries
  # so we can send them as json objects later
  for i in range(len(chain_to_send)):
    block = chain_to_send[i]
    block_index = str(block.index)
    block_timestamp = str(block.timestamp)
    block_data = str(block.data)
    block_hash = block.hash
    chain_to_send[i] = {
      "index": block_index,
      "timestamp": block_timestamp,
      "data": block_data,
      "hash": block_hash
    }
  chain_to_send = json.dumps(chain_to_send)
  return chain_to_send

def find_new_chains():
  # Get the blockchains of every
  # other node
  other_chains = []
  for node_url in peer_nodes:
    # Get their chains using a GET request
    block = requests.get(node_url + "/blocks").content
    # Convert the JSON object to a Python dictionary
    block = json.loads(block)
    # Add it to our list
    other_chains.append(block)
  return other_chains

def consensus():
  # Get the blocks from other nodes
  other_chains = find_new_chains()
  # If our chain isn't longest,
  # then we store the longest chain
  longest_chain = blockchain
  for chain in other_chains:
    if len(longest_chain) < len(chain):
      longest_chain = chain
  # If the longest chain isn't ours,
  # then we stop mining and set
  # our chain to the longest one
  blockchain = longest_chain

def proof_of_work(last_proof):
  # Create a variable that we will use to find
  # our next proof of work
  incrementor = last_proof + 1
  # Keep incrementing the incrementor until
  # it's equal to a number divisible by 9
  # and the proof of work of the previous
  # block in the chain
  while not (incrementor % 9 == 0 and incrementor % last_proof == 0):
    incrementor += 1
  # Once that number is found,
  # we can return it as a proof
  # of our work
  return incrementor

@node.route('/mine', methods = ['GET'])
def mine():
  # Get the last proof of work
  last_block = blockchain[len(blockchain) - 1]
  last_proof = last_block.data['proof-of-work']
  # Find the proof of work for
  # the current block being mined
  # Note: The program will hang here until a new
  #       proof of work is found
  proof = proof_of_work(last_proof)
  # Once we find a valid proof of work,
  # we know we can mine a block so
  # we reward the miner by adding a transaction
  this_nodes_transactions.append(
    { "from": "network", "to": miner_address, "amount": 1 }
  )
  # Now we can gather the data needed
  # to create the new block
  new_block_data = {
    "proof-of-work": proof,
    "transactions": list(this_nodes_transactions)
  }
  new_block_index = last_block.index + 1
  new_block_timestamp = this_timestamp = date.datetime.now()
  last_block_hash = last_block.hash
  # Empty transaction list
  this_nodes_transactions[:] = []
  # Now create the
  # new block!
  mined_block = Block(
    new_block_index,
    new_block_timestamp,
    new_block_data,
    last_block_hash
  )
  blockchain.append(mined_block)
  # Let the client know we mined a block
  return json.dumps({
      "index": new_block_index,
      "timestamp": str(new_block_timestamp),
      "data": new_block_data,
      "hash": last_block_hash
  }) + "\n"

node.run()

C:\Users\cesar\OneDrive - stevens.edu\Spring 2023 (3rd Year)\EE-322 D6\iot\lesson10>python snakecoin-server-full-code.py
 * Serving Flask app 'snakecoin-server-full-code'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on http://127.0.0.1:5000
Press CTRL+C to quit
```
 ### I then navigated to http://127.0.0.1:5000 and it displayed the following: ###
 ![image](https://user-images.githubusercontent.com/91222019/236381631-7c42b09b-9a08-4451-afef-c44bd0b9adad.png)

### On terminal 2, I executed the desired code and got the following: ###
![image](https://user-images.githubusercontent.com/91222019/236382330-b3d3dd0b-459e-444a-8ca5-ea610339e60d.png)


