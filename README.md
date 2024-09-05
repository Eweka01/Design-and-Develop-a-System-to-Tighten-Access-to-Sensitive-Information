
# User Role Management System

This project implements a simple role management system using a cache-like structure. Each user can have a limited number of active roles, and when a new role is added after reaching the limit, the oldest role is removed.

## Features
- **Role management**: Keeps track of user roles, allowing a fixed number of active roles at a time.
- **Role updates**: If a role already exists, its message is updated, and it is marked as recently used.
- **Eviction policy**: When the role limit is reached, the least recently used role is evicted to make space for new roles.
  
## Methods
### `__init__(self, capacity)`
Initializes the system with a given `capacity` to manage the maximum number of roles allowed.

### `get(self, role)`
Retrieves the message for a specific role. Moves the role to the most recent position.

### `set(self, role, message)`
Adds or updates a role and its corresponding message. If the cache is full, the oldest role is removed.

### `_complexity(self)`
Provides the runtime complexity of the `get` and `set` methods, along with the space complexity.

## Complexity
- **Time complexity (get and set)**: O(1)
- **Space complexity**: O(N), where N is the number of roles.

## Dependencies
- Python 3.x
- `collections.OrderedDict`

