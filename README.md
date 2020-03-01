# Demo of User Access Management in Kubernetes with Keycloak and FreeIPA

This repository contains the demo setup for the talk at Sec4Dev 2020.

## Prerequisites

To run this demo you need the following:

- Docker & Docker Compose
- some Kubernetes Cluster(s)
- maybe some real domain and a LE certificate (if you like HTTPS and the green lock in the URL bar :))
- kubectl
- [kubelogin](https://github.com/WhizUs/kubelogin)

## Run

0. If you have imported the demo realm, recreate the client secrets, type in the IPA admin key and you're done!
1. Login in Keycloak
2. Add new realm, f.e. "demo" 
3. In "User Federation" select "ldap" and add a new configuration (name it demo f.e.)
4. Fill in the fields for the connection and group mappings :)
5. Login in FreeIPA
6. Add users and groups and users to groups!
7. Go back to Keycloak --> demo realm --> user federation --> demo -> sync users
8. Add kubectl and kubernetes clients
9. Copy kubectl client secret
10. Use kubectl config template and fill in the client secret
11. Configure the kube-apiserver to use keycloak with kubernetes client
12. Login using kubelogin!