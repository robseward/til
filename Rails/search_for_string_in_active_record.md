# Search for an object with a partial string

`Artwork.where("title LIKE ?", "%bar%")`

Will match items whose title contains "bar," such as "foo bar" and "bar baz."
