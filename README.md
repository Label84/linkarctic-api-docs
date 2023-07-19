# LinkArctic API

- [Introduction](#introduction)
- [API](#API)
  - [API Base Endpoint](#api-base-endpoint)
  - [API Authentication](#api-authentication)
- [Endpoints](#endpoints)
  - [Bookmarks](#bookmarks)
    - [List bookmarks](#list-bookmarks)
    - [Get bookmark](#get-bookmark)
    - [Create bookmark](#create-bookmark)
    - [Update bookmark](#update-bookmark)
    - [Delete bookmark](#delete-bookmark)
  - [Categories](#categories)
    - [List categories](#list-categories)
    - [Get category](#get-category)
    - [Create category](#create-category)
    - [Update category](#update-category)
    - [Delete category](#delete-category)
  - [Bookmark Category](#bookmark-category)
    - [Attach category](#attach-category)
    - [Detach category](#detach-category)

## Introduction

This document describes the API endpoints for [LinkArctic](https://linkarctic.com).

## API

### API Base Endpoint

Endpoint: `https://linkarctic.com/api/v1`

### API Authentication

When making a requests, the API token should be included in the Authorization header as a Bearer token.

You can obtain your API token on your 'Account' page [https://linkarctic.com/account](https://linkarctic.com/account).

## Endpoints

### Bookmarks

- [List bookmarks](#list-bookmarks)
- [Get bookmark](#get-bookmark)
- [Create bookmark](#create-bookmark)
- [Update bookmark](#update-bookmark)
- [Delete bookmark](#delete-bookmark)

#### List bookmarks

Retrieve all bookmarks.

Endpoint: `GET` `/api/v1/bookmarks`

#### Get bookmark

Retrieve a single bookmark by its UUID.

Endpoint: `GET` `/api/v1/bookmarks/{uuid}`

#### Create bookmark

Creates a bookmark.

Endpoint: `POST` `/api/v1/bookmarks`

#### Update bookmark

Update an existing bookmark.

Endpoint: `PUT/PATCH` `/api/v1/bookmarks/{uuid}`

#### Delete bookmark

Delete a bookmark. All links created for this bookmark will be deleted as well.

Endpoint: `DELETE` `/api/v1/bookmarks/{uuid}`

### Categories

- [List categories](#list-categories)
- [Get category](#get-category)
- [Create category](#create-category)
- [Update category](#update-category)
- [Delete category](#delete-category)

#### List categories

Retrieve all categories.

Endpoint: `GET` `/api/v1/categories`

#### Get category

Retrieve a single category by its UUID.

Endpoint: `GET` `/api/v1/categories/{uuid}`

#### Create category

Creates a category.

Endpoint: `POST` `/api/v1/categories`

#### Update category

Update an existing category.

Endpoint: `PUT/PATCH` `/api/v1/categories/{uuid}`

#### Delete category

Delete a category. This will not impact any bookmark that have this category attached.

Endpoint: `DELETE` `/api/v1/categories/{uuid}`

### Bookmark Category

- [Attach category](#attach-category)
- [Detach category](#detach-category)

#### Attach category

Attach a category to a bookmark.

Endpoint: `PUT/PATCH` `/api/v1/bookmarks/{uuid}/categories/{uuid}`

#### Detach category

Detach a category from a bookmark.

Endpoint: `PUT/PATCH` `/api/v1/bookmarks/{uuid}/categories/{uuid}`

