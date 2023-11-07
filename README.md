# LinkArctic API

- [Introduction](#introduction)
- [API](#api)
  - [API Base Endpoint](#api-base-endpoint)
  - [API Authentication](#api-authentication)
- Endpoints
  - [Boards](./endpoints/boards.md)
    - [List boards](./endpoints/boards.md#list-boards)
    - [Get board](./endpoints/boards.md#get-board)
    - [Create board](./endpoints/boards.md#create-board)
    - [Update board](./endpoints/boards.md#update-board)
    - [Delete board](./endpoints/boards.md#delete-board)
  - [Bookmarks](./endpoints/bookmarks.md)
    - [List bookmarks](./endpoints/bookmarks.md#list-bookmarks)
    - [Get bookmark](./endpoints/bookmarks.md#get-bookmark)
    - [Create bookmark](./endpoints/bookmarks.md#create-bookmark)
    - [Update bookmark](./endpoints/bookmarks.md#update-bookmark)
    - [Delete bookmark](./endpoints/bookmarks.md#delete-bookmark)
  - [Categories](./endpoints/categories.md)
    - [List categories](./endpoints/categories.md#list-categories)
    - [Get category](./endpoints/categories.md#get-category)
    - [Create category](./endpoints/categories.md#create-category)
    - [Update category](./endpoints/categories.md#update-category)
    - [Delete category](./endpoints/categories.md#delete-category)
  - [Bookmark Category](./endpoints/bookmark-category)
    - [Attach category](./endpoints/bookmark-category.md#attach-category)
    - [Detach category](./endpoints/bookmark-category.md#detach-category)
- [Contact](#contact)

## Introduction

This document describes the API endpoints for [LinkArctic](https://linkarctic.com).

A basic bookmarking tool to collect and organize your favorite websites and notes. Loads fast. Easy to use.

- `Board` a workspace where you can create bookmarks and categories (Example 'Project A')
- `Bookmark` a note/description/url basically anything (Example  a link to '[Taylor Swift - You Belong With Me - YouTube](https://www.youtube.com/watch?v=VuNIsY6JdUw)')
- `Category` to group bookmarks you can attach them to a category (Example 'YouTube')

## API

### API Base Endpoint

Endpoint: `https://linkarctic.com/api/v1`

### API Authentication

When making a requests, the API token should be included in the Authorization header as a `Bearer token`.

You can obtain your API token on your 'Account' page [https://linkarctic.com](https://linkarctic.com).

You can only access the boards that are bound to your API token. In case you get an `403 Forbidden` response, you are probably trying to access a board that is not bound to your API token. You can also create a 'wildcard' token - that allows you to access all boards.

## Contact

For more information you can send an email to [info@label84.com](info@label84.com).

Feel free to create an issue or PR if you see any errors of inconsistencies.
