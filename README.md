# Express.js JSON Body Parsing Issue

This repository demonstrates a common issue encountered when working with JSON request bodies in Express.js applications. The problem arises when the request body is not parsed correctly due to missing or incorrect `Content-Type` header in the request.

## Bug Description

The provided Express.js application attempts to handle POST requests to the `/user` endpoint.  It expects a JSON payload, but fails to parse it if the client doesn't set the `Content-Type` header to `application/json`.  This results in `req.body` being empty.

## Bug Solution

A solution involves adding a middleware function to explicitly parse JSON data from the request body even if the header is absent or wrong.