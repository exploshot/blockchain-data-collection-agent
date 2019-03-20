# Qwertycoin fork of TurtlePay™ Blockchain Data Collection Agent (BDCA)

[![NPM](https://nodei.co/npm/qwertycoin-bdca.png?downloads=true&stars=true)](https://nodei.co/npm/qwertycoin-bdca/)

#### Master Build Status
[![Build Status](https://travis-ci.org/qwertycoin-org/blockchain-data-collection-agent.svg?branch=master)](https://travis-ci.org/qwertycoin-org/blockchain-data-collection-agent) [![Build status](https://ci.appveyor.com/api/projects/status/github/qwertycoin-org/blockchain-data-collection-agent?branch=master&svg=true)](https://ci.appveyor.com/project/qwertycoin-org/blockchain-data-collection-agent/branch/master)

## Prerequisites

* [Qwertycoin](https://github.com/qwertycoin-org/qwertycoin)
* MariaDB/MySQL with InnoDB support
* [Node.js](https://nodejs.org/) LTS

## Foreword

We know that this documentation needs cleaned up and made easier to read. We'll compile it as part of the full documentation as the project works forward.

## Setup

1) Clone this repository to wherever you'd like as long as it can communicate with your SQL server to run:

```bash
git clone https://github.com/qwertycoin-org/blockchain-data-collection-agent
```

2) Install the required Node.js modules

```bash
cd blockchain-data-collection-agent && npm install
```

3) Load the database schema from `schema.sql` into your configured database.

4) Fire up the script

```bash
export MYSQL_HOST=localhost
export MYSQL_PORT=3306
export MYSQL_USERNAME=yourdbusername
export MYSQL_PASSWORD=yourdbpassword
export MYSQL_DATABASE=yourdbname
export NODE_HOST=localhost
export NODE_PORT=11898
node index.js	node index.js
```	```

5) Optionally, install PM2 or another process manager to keep the service running.

```bash
npm install -g pm2@latest
pm2 startup
pm2 start index.js --name blockchain-data-collection-agent
pm2 save
```

6) Wait to build your database cache (this is likely to take days depending on the size of your chain)

###### (c) 2018-2019 TurtlePay™ Development Team
