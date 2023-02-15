# Simultaneous-async-parallel-operations

// In parallel
async function getFriendPosts(user) {
 friendIds = await.db.get("friends", {user}, {id: 1});
 friendPosts = await Promise.all( friendIds.map(id =>
 db.get("posts", {user: id})
 );
 // etc.
}
