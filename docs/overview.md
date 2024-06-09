---
layout: page
---

# Overview

Welcome to Visual Chronicle. This is a mock API service that simulates REST interface for an imaginary cloud-hosted tool in which users can log movies they've seen. Subscribers can register users, post movies, and add log dates. This page provides an overview of some of the tool's features, as well as some quickstart ideas.

## Key Features

### User Database

The user resource is an endpoint that allows users to be created for the service. Each user has identifying properties of their name, a unique email address and an ID. The user resource can be updated or deleted as necessary.

### Movie Archive

The movie resource is an endpoint that allows a user to post a movie, search for a movie, or retrieve all movies. Movies have several identifying properties including their title, release year, and director.

### Watch History

Once a user and a movie are added to the service, user's can assign a watch history to any movie. This resource tracks the date the movie was watched and where it was watched. It also has a unique ID.

## Quick Links

- [Quickstart](index#quickstart)
- [Tutorial: Enroll a new user](tutorials/tutorial-enroll-user)
- [Tutorial: Post a new moie](tutorials/tutorial-add-movie)
- [Tutorial: Add a new watch history](tutorials/tutorial-add-watch-history)
- [API Reference Docs](index#visual-chronicle-api)
