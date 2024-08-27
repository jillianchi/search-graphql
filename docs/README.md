# Search GraphQL

Forked from vtex.search-graphql@0.62.0. Main changes: Add CHEAPEST_AVAILABLE to type ItemsFilter in graphql/types/Product.graphql.


BEFORE
graphql/types/Product.graphql

enum ItemsFilter {
 """
 Returns all items, same as no filter.
 """
 ALL
 """
 Returns only the first available item. Returns first if no item is available.
 """
 FIRST_AVAILABLE
 """
 Returns all available items. Returns first if no item is available.
 """
 ALL_AVAILABLE
}


AFTER
graphql/types/Product.graphql

enum ItemsFilter {
 """
 Returns all items, same as no filter.
 """
 ALL
 """
 Returns only the first available item. Returns first if no item is available.
 """
 FIRST_AVAILABLE
 """
 Returns all available items. Returns first if no item is available.
 """
 ALL_AVAILABLE
 """
 Returns the cheapest available item. Returns first if no item is available.
 """
 CHEAPEST_AVAILABLE
}

