+++
categories = ["web-dev"]
coders = []
date = 2019-12-20T23:00:00Z
description = "A distributed user database implementing the chord using gRPC and protobufs"
github = ["https://github.com/bushidocodes/chord-grpc"]
image = "https://res.cloudinary.com/aalbero/image/upload/v1597341297/Chord_network_ymg0nn.png"
title = "Distributed User Database"
type = "post"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597260172/nodejs_tsvkve.svg"
name = "Node.js"
url = "https://nodejs.org/en/"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597341192/grpc_emgilo.png"
name = "gRPC"
url = "https://grpc.io/"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597341110/protobuf_r5eb6a.png"
name = "Protocol Buffers"
url = "https://developers.google.com/protocol-buffers"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597341297/Chord_network_ymg0nn.png"
name = "Chord Algorithm"
url = "https://pdos.csail.mit.edu/papers/ton:chord/paper-ton.pdf"
+++

### [Clik here to watch a Demo](https://www.youtube.com/watch?v=x2AixjsanyE)

## Description
This project is an implementation of a p2p distributed hash table using the Chord algorithm by Ion Stoica, Robert Morris, David Karger, Kaashoek, and Hari Balakrishnan. It uses Node.js to implement the nodes, and gRPC as the method of inter-node communiation.

The client script:
- runs a crawler that walks the Chord successor chain to build an in-memory representaiton of the state of the overlay network
- serves a simple web UI that visualizes the overlay network

In the future, the project will implement a "Stack Exchange Computer Science User Service" on top of this DHT, complete with a simple web app to demonstrate transparency and real-work use of a DHT. It will also enhance the admin pain to add controls to dynamically add and remove nodes from the Chord.

You can go to the GitHub page for more details.
You can find a video demo performed by my classmate Sean in the following link: https://www.youtube.com/watch?v=x2AixjsanyE