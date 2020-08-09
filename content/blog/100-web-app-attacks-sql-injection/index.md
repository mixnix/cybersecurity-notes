---
title: 100 web app attacks: sql injection
date: "2020-08-09T21:02:03.284Z"
description: Instruction how to detect sql injection vulnerability and execute it
---

## Sql injection

Sql injection is an attack that works when web application passes non-sanitized input to database from frontend input 
(for example forms)

How to detect vulnerability: 
- go through initial recon: detect all inputs (text-inputs, forms)
- check if server throws sql error when ' is entered through input and sent to backend
- if server throws sql error or you want to do blind attack then use burp suite to enumerate target input with
attack checklist from this github
https://github.com/fuzzdb-project/fuzzdb/blob/master/attack/sql-injection/detect/xplatform.txt
- when there is 200 response you can assume that this request works	
- depending on how vulnerable the server is you can use this request to log in, get data from database or delete it
