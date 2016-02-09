# graphql-cheat-sheet
Useful snippets for working with graphql/relay


## GraphiQL

### Mutations

```
mutation example($likePost: LikePostInput!){
  likePost(input: $likePost) {
    post {
      likeCount
    }
    viewer {
      viewerHasLiked
    }
  }
}
```
and in the *variables* panel:
```
{
  "likePost": {
    "clientMutationId": "some-client-mutation-id",
    "postId": "some-post-id"
  }
}
```
