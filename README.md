# Minimal Blockchain Implementation

Blockchain implementation using Python based off [this](https://hackernoon.com/learn-blockchains-by-building-one-117428612f46) article.

### Getting Started
- Start nodes `python blockchain.py <PORT>`
- Each node should register their neighbours

### Endpoints
- `GET /chain`: Get the node's version of the chain
- `GET /mine`: Mine the next block
- `GET /nodes/resolve`: Apply the consensus algorithm
- `POST /nodes/register`: Register neighbours
  - `req.body.nodes`: List of node URLs
- `POST /transactions/new`: Create a transction to be added to the next block
  - `req.body.sender`: Sender's UUID
  - `req.body.recipient`: Recipients UUID
  - `req.body.amount`: Amount to transfer

### TODO
- Nodes should able to retrieve info i.e. UUID, balance
- Consensus need not be manually triggered i.e. done during `GET /chain`
- Disallow mining of empty Blocks
- Add a nice UI