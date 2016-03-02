Basecamps
=========

**Projects are now called Basecamps in Basecamp 3.** However, the URLs use "projects" still.

Endpoints:

- [Get Basecamps](#get-basecamps)
- [Get a Basecamp](#get-a-basecamp)
- [Create a Basecamp](#create-a-basecamp)
- [Update a Basecamp](#update-a-basecamp)
- [Trash a Basecamp](#trash-a-basecamp)

Get Basecamps
-------------

* `GET /projects.json` will return all active Basecamps visible to the current user.
* `GET /projects/archive.json` will return all archived Basecamps visible to the current user.
* `GET /projects/trash.json` will return all trashed Basecamps visible to the current user.

```json
[
   {
      "vault_url" : "https://3.basecamp.com/195539477/buckets/2085958495/vaults/9007199254741021",
      "id" : 2085958495,
      "bookmark_url" : "https://3.basecamp.com/195539477/my/bookmarks/BAh7CEkiCGdpZAY6BkVUSSIrZ2lkOi8vYmMzL0J1Y2tldC8yMDg1OTU4NDk1P2V4cGlyZXNfaW4GOwBUSSIMcHVycG9zZQY7AFRJIg1yZWFkYWJsZQY7AFRJIg9leHBpcmVzX2F0BjsAVDA=--06a5145963152c63ea56090695ec59e6d83fb21a",
      "created_at" : "2016-01-27T11:00:20.701-06:00",
      "name" : "Annie's Corner",
      "updated_at" : "2016-02-11T09:49:52.878-06:00",
      "status" : "active",
      "description" : "Annie's Stuff. Keep Out. 😁",
      "bookmarked" : false,
      "url" : "https://3.basecamp.com/195539477/projects/2085958495"
   },
   {
      "name" : "Honcho Design Newsroom",
      "created_at" : "2016-01-27T11:00:28.325-06:00",
      "bookmark_url" : "https://3.basecamp.com/195539477/my/bookmarks/BAh7CEkiCGdpZAY6BkVUSSIrZ2lkOi8vYmMzL0J1Y2tldC8yMDg1OTU4NDk2P2V4cGlyZXNfaW4GOwBUSSIMcHVycG9zZQY7AFRJIg1yZWFkYWJsZQY7AFRJIg9leHBpcmVzX2F0BjsAVDA=--456eaced982bc4da97ac830c019a4af1d250bb21",
      "vault_url" : "https://3.basecamp.com/195539477/buckets/2085958496/vaults/9007199254741052",
      "id" : 2085958496,
      "url" : "https://3.basecamp.com/195539477/projects/2085958496",
      "bookmarked" : false,
      "status" : "active",
      "description" : "Let's talk about the company!",
      "updated_at" : "2016-02-09T22:40:55.279-06:00"
   },
   {
      "status" : "active",
      "description" : "Looking for the best!",
      "updated_at" : "2016-02-11T09:49:55.177-06:00",
      "url" : "https://3.basecamp.com/195539477/projects/2085958497",
      "bookmarked" : false,
      "bookmark_url" : "https://3.basecamp.com/195539477/my/bookmarks/BAh7CEkiCGdpZAY6BkVUSSIrZ2lkOi8vYmMzL0J1Y2tldC8yMDg1OTU4NDk3P2V4cGlyZXNfaW4GOwBUSSIMcHVycG9zZQY7AFRJIg1yZWFkYWJsZQY7AFRJIg9leHBpcmVzX2F0BjsAVDA=--9a7b024a94ef1e7abaa92676ceb712dff9de6885",
      "created_at" : "2016-01-27T11:01:58.074-06:00",
      "vault_url" : "https://3.basecamp.com/195539477/buckets/2085958497/vaults/9007199254741364",
      "id" : 2085958497,
      "name" : "Honcho Recruiting and Hiring"
   },
   {
      "name" : "The Leto Laptop",
      "created_at" : "2016-01-27T11:02:32.061-06:00",
      "bookmark_url" : "https://3.basecamp.com/195539477/my/bookmarks/BAh7CEkiCGdpZAY6BkVUSSIrZ2lkOi8vYmMzL0J1Y2tldC8yMDg1OTU4NDk4P2V4cGlyZXNfaW4GOwBUSSIMcHVycG9zZQY7AFRJIg1yZWFkYWJsZQY7AFRJIg9leHBpcmVzX2F0BjsAVDA=--c8e1a465de900eb9864fa79ae2f30345be158f71",
      "vault_url" : "https://3.basecamp.com/195539477/buckets/2085958498/vaults/9007199254741442",
      "id" : 2085958498,
      "url" : "https://3.basecamp.com/195539477/projects/2085958498",
      "bookmarked" : false,
      "status" : "active",
      "description" : "Laptop product launch.",
      "updated_at" : "2016-01-27T11:03:32.570-06:00"
   }
]
```

###### Copy as cURL:

``` shell
curl -s -H "Authorization: Bearer $ACCESS_TOKEN" https://3.basecamp.com/$ACCOUNT_ID/projects.json
```


Get a Basecamp
--------------

* `GET /projects/1.json` will return the Basecamp with the given ID, granted they have access to it.


``` json
{
   "bookmark_url" : "https://3.basecamp.com/195539477/my/bookmarks/BAh7CEkiCGdpZAY6BkVUSSIrZ2lkOi8vYmMzL0J1Y2tldC8yMDg1OTU4NDk2P2V4cGlyZXNfaW4GOwBUSSIMcHVycG9zZQY7AFRJIg1yZWFkYWJsZQY7AFRJIg9leHBpcmVzX2F0BjsAVDA=--456eaced982bc4da97ac830c019a4af1d250bb21",
   "created_at" : "2016-01-27T11:00:28.325-06:00",
   "updated_at" : "2016-02-09T22:40:55.279-06:00",
   "vault_url" : "https://3.basecamp.com/195539477/buckets/2085958496/vaults/9007199254741052",
   "url" : "https://3.basecamp.com/195539477/projects/2085958496",
   "id" : 2085958496,
   "name" : "Honcho Design Newsroom",
   "description" : "Let's talk about the company!",
   "status" : "active"
}
```

###### Copy as cURL:

``` shell
curl -s -H "Authorization: Bearer $ACCESS_TOKEN" https://3.basecamp.com/$ACCOUNT_ID/projects/1.json
```


Create a Basecamp
-----------------

* `POST /projects.json` with at least a name, and optionally a description, to kick off a new Basecamp.

``` json
{
  "name": "Marketing Campaign",
  "description": "For Client: Xyz Corp Conference"
}
```

This will return `201 Created` with the current JSON representation of the Basecamp if the creation was a success. See the [Get a Basecamp](#get-a-basecamp) endpoint for more info. If the account has reached the Basecamp limit you'll see a `507 Insufficient Storage` and a response of:

``` json
{
  "error": "The Basecamp limit for this account has been reached."
}
```

If you hit that error, you'll need to either archive or trash projects, or upgrade your subscription to a bigger plan. After creating a Basecamp, you'll  want to [allow people to get in][1]. Or maybe, [add some to-dos][2]?

###### Copy as cURL:

``` shell
curl -s -H "Authorization: Bearer $ACCESS_TOKEN" -H "Content-Type: application/json" \
  -d '{"name":"Marketing Campaign","description":"For Client: Xyz Corp Conference"}' \
  https://3.basecamp.com/$ACCOUNT_ID/projects.json
```


Update a Basecamp
-----------------

* `PUT /projects/1.json` will allow updating of a Basecamp's name and description.

``` json
{
  "name": "Marketing Campaign for Xyz Corp",
  "description": "2016-2017 Strategy"
}
```

This will return `204 No Content` when successful. See the [Get a Basecamp](#get-a-basecamp) endpoint for more info.

###### Copy as cURL:

``` shell
curl -s -H "Authorization: Bearer $ACCESS_TOKEN" -H "Content-Type: application/json" \
  -d '{"name":"Marketing Campaign for Xyz Corp","description":"2016-2017 Strategy"}' -X PUT \
  https://3.basecamp.com/$ACCOUNT_ID/projects/2085958506.json
```


Trash a Basecamp
----------------

* `DELETE /projects/1.json` will mark the Basecamp with the given ID as trashed.

Trashed Basecamps will be deleted from Basecamp 3 after 30 days. No parameters required. Returns `204 No Content` if successful.

###### Copy as cURL:

``` shell
curl -s -H "Authorization: Bearer $ACCESS_TOKEN" -H "Content-Type: application/json" -X DELETE \
  http://bc3.dev/$ACCOUNT_ID/projects/2085958507.json
```

[1]: https://github.com/basecamp/bc3-api/blob/master/sections/accesses.md#accesses
[2]: https://github.com/basecamp/bc3-api/blob/master/sections/todos.md#todos