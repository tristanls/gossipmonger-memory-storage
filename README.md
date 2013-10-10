# gossipmonger-memory-storage

_Stability: 1 - [Experimental](https://github.com/tristanls/stability-index#stability-1---experimental)_

[![NPM version](https://badge.fury.io/js/gossipmonger-memory-storage.png)](http://npmjs.org/package/gossipmonger-memory-storage)

An in-memory storage engine for [Gossipmonger](https://github.com/tristanls/node-gossipmonger) (an implementation of the Scuttlebutt gossip protocol endpoint for real-time peer-to-peer replication).

## Installation

    npm install gossipmonger-memory-storage

## Tests

    npm test

_NOTE: There are no tests right now._

## Overview

Minimalistic default in-memory storage engine for [Gossipmonger](https://github.com/tristanls/node-gossipmonger).

## Documentation

### MemoryStorage

**Public API**

  * [new MemoryStorage()](#new-memorystorage)
  * [memoryStorage.deadPeers()](#memorystoragedeadpeers)
  * [memoryStorage.get(id)](#memorystoragegetid)
  * [memoryStorage.livePeers()](#memorystoragelivepeers)
  * [memoryStorage.put(id, peer)](#memorystorageputid-peer)

#### new MemoryStorage()

Creates a new MemoryStorage instance.

#### memoryStorage.deadPeers()

  * Return: _Array_ An array of peers that are dead (`peer.live != true`).

#### memoryStorage.get(id)

  * `id`: _String_ Id of peer to get.
  * Return: _Object_ Peer with given `id` or `undefined`.

#### memoryStorage.livePeers()

  * Return: _Array_ An array of peers that are live (`peer.live == true`).

#### memoryStorage.put(id, peer)

  * `id`: _String_ Id of peer to put.
  * `peer`: _Object_ Peer to put into storage.