# Shopping List (Supabase User Aware App)

Use [this template](https://github.com/alchemycodelab/web-template-supabase) for this deliverable.

## Demo

[Live Demo](https://web-shopping-list-supabase.netlify.app/)

## Supabase

- Create a new supabase project
- Turn on email authentication, but no email confirmation

## Data Model(s)

`list` table:

Supabase creates these by default:

- `id` primary key
- `created_at` timestamp

Also add:

- `item` varchar (not nullable)
- `quantity`  int8 (nullable)
- `bought` boolean default false (nullable)
- `user_id` uuid linked to `users` table `id` column

## Requirements

### Features

- Auth (comes with template)
- Users should be able to add items to their shopping list (CREATE)
- Users should see a list of shopping items (READ)
- Users should be able to mark items as bought (UPDATE)
- Users should be able to delete all the items from their list (DELETE)

### Authentication

Enable RLS for the table so:

- Users only see their own data
- Users can only update the data to their own user_id

## Rubric

The following is required for your assignment to be graded:
- PR open from `dev` to `main`
- PR Passes CI (lint + tests)
- PR preview on netlify

| Commits with Working Features...                           | Points |
| ---------------------------------------------------------- | ------ |
| Users should be able to add items to their shopping list (CREATE)                     | 5 |
| Users should see a list of shopping items (READ)                      | 5 |
| Users should be able to mark items as bought (UPDATE)                     | 5 |
| Users should be able to delete all the items from their list (DELETE)                     | 5 |
