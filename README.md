# WP Objectly Timber

This is the timber extension for WP Objectly, and provides functionality so you can easier integrate WP Objectly with Timber.

This extension provides functionality for PostObject and PostObjectQueryBuilder under the namespace `->timber` and `::timber()`

# PostObject
## toTimberPost()
Get a WP Objectly PostObject as a timber post

```php
$post = Post::formPostID(1);
$timberPost = $post->timber->toTimberPost();
```

# QueryBuilder
## run
Run a query to get timber posts as output, instead of WP Objectly PostObject's

```php
$timberPosts = Post::get()
    ->fromAuthor(User::fromUserID(1))
    ->withTerm(CategoryTerm::fromTermSlug('my-cat')
    ->timber->run(); // <-- Get timber posts instead of WP Objectly posts