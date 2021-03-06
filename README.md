# duco

DUCO (Duino Coin) is a cryptocurrency created to be mined on small low powered, low cost devices such as Arduino (hence (Ar)**Duino** Coin). More about the coin can be found on the [website](https://duinocoin.com).

This is a simple Python package that helps you connect to the REST API, allowing you to get all data about current miners, balances, transactions, and server statistics.

## Installation

`python3 -m pip install duco`

## Usage

```python
from duco import DUCO

d = DUCO()

balances = d.fetch_balances()

```

### Fetch Miners

* **Description:** 
  The function used to retrieve all miners from the REST API.

* **Signature:**
   `fetch_miners(self, filters: List[Filter] = None)`

* **Arguments:**
   - `filters`: a list of `Filter` objects used to narrow down results. (Optional)
 - **Returns:**

### Fetch Miner

* **Description:**
  The function used to retrieve a single miner by it's `threadid` from the REST API.
* **Signature:**
  `def fetch_miner(self, threadid: str)`
* **Arguments:**
  \- `threadid`: the thread id of the miner you wish to get
* **Returns:**
  \- a `Miner` object

### Fetch Transactions

* **Description:**
  The function used to retrieve all transactions from the REST API.
* **Signature:**
  `def fetch_transactions(self, filters: List[Filter] = None, sort: Sort = None, limit: Limit = None)`
* **Arguments:**
  \- `filters`: a list of `Filter` objects used to narrow down results. (Optional)
  \- `sort`: a single `Sort` object detailing how the response should be sorted. (Optional)
  \- `limit`: a single `Limit` object detailing how many objects should be in the response. (Optional)
* **Returns:**
  \- a list of `Transaction` objects

### Fetch Transaction

* **Description:**
  The function used to retrieve a single transaction by it's `hash` from the REST API.
* **Signature:**
  `def fetch_transaction(self, hash_id: str)`
* **Arguments:**
  \- `hash_id`: the hash of the transaction you wish to get
* **Returns:**
  \- a `Transaction` object

### Fetch Balances

* **Description:**
  The function used to retrieve all balances from the REST API.

* **Signature:**

  `def fetch_balances(self, filters: List[Filter] = None, sort: Sort = None, limit: Limit = None)`

* **Arguments:**
  \- `filters`: a list of `Filter` objects used to narrow down results. (Optional)
  \- `sort`: a single `Sort` object detailing how the response should be sorted. (Optional)
  \- `limit`: a single `Limit` object detailing how many objects should be in the response. (Optional)

* **Returns:**
  \- a list of `Balance` objects

### Fetch Balance

* **Description:**
  The function used to retrieve a single balance for a user from the REST API.
* **Signature:**
  `def fetch_balance(self, username: str)`
* **Arguments:**
  \- `username`: the username of the balance you wish to get
* **Returns:**
  \- a `Balance` object

### Fetch Statistics

* **Description:**
  The function used to retrieve the statistics from the REST API.
* **Signature:**
  `def fetch_statistics(self)`
* **Returns:**
  \- a `Statistics` object

