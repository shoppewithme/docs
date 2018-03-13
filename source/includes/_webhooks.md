# Webhooks

This is a list of all the types of events we currently send. We may add more at any time, so you shouldn't rely on only these types existing in your code.

You'll notice that these events follow a pattern: resource.event. Our goal is to design a consistent system that makes things easier to anticipate and code against.


Event | Description
---------- | -------
item.created | Occurs whenever an item is created
item.updated | Occurs whenever an item is updated
item.deleted | Occurs whenever an item is deleted
popup.created | Occurs whenever a popup is created
popup.updated | Occurs whenever a popup is updated
popup.deleted | Occurs whenever a popup is deleted
lives.created | Occurs whenever a live is created
lives.updated | Occurs whenever a live is updated
lives.deleted | Occurs whenever a live is deleted
albums.created | Occurs whenever an album is created
albums.updated | Occurs whenever an album is updated
albums.deleted | Occurs whenever an album is deleted