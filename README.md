# LinkArctic API

- [Introduction](#introduction)
- [API](#api)
  - [API Base Endpoint](#api-base-endpoint)
  - [API Authentication](#api-authentication)
- [Endpoints](./endpoints/bookmarks.md)
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

## API

### API Base Endpoint

Endpoint: `https://linkarctic.com/api/v1`

### API Authentication

When making a requests, the API token should be included in the Authorization header as a `Bearer token`.

You can obtain your API token on your 'Account' page [https://linkarctic.com/account](https://linkarctic.com/account).

## Contact

For more information you can send an email to [info@label84.com](info@label84.com).

Feel free to create an issue or PR if you see any errors of inconsistencies.
