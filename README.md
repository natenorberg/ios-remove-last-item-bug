# ios-remove-last-item-bug
Basic repo to reproduce an issue I was seeing with master/detail views in SwiftUI

# The Problem

If you have a SwiftUI master-detail app and provide a way to remove an item from the detail view, you get in a weird navigation state if you try to remove the last item. I started with a brand new iOS "Master-Detail App" template and just added enough to reproduce this issue.

# Expected Behavior
1. Click the + button to add some items to the list
1. Select an item to switch to the detail view
1. Press delete
1. The item is removed from the list and you are redirected back to the list

# Current Behavior
Everything behaves as expected if you do this with any item other than the very last one

However, if you delete the last item from the detail view, the item is removed from the list, but you aren't navigated back. You just stay on the detail view. There aren't any console errors.

There seems to be some gotcha here that I'm not aware of.
