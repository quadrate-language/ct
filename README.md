# ct

Container types module for Quadrate.

## Installation

```bash
quadpm install ct
```

## Containers

### vec - Dynamic Array

```qd
use ct

fn main() {
    ct::vec::new -> v
    v 10 ct::vec::push
    v 20 ct::vec::push
    v ct::vec::len print nl  // 2
    v 0 ct::vec::get print nl  // 10
}
```

### hashmap - Hash Map

```qd
use ct

fn main() {
    ct::hashmap::new -> m
    m "key" "value" ct::hashmap::set
    m "key" ct::hashmap::get -> val found
    found if { val print nl }
}
```

### set - Hash Set

```qd
use ct

fn main() {
    ct::set::new -> s
    s "apple" ct::set::add
    s "banana" ct::set::add
    s "apple" ct::set::contains print nl  // 1
}
```

### queue - FIFO Queue

```qd
use ct

fn main() {
    ct::queue::new -> q
    q 1 ct::queue::enqueue
    q 2 ct::queue::enqueue
    q ct::queue::dequeue print nl  // 1
}
```

### deque - Double-Ended Queue

```qd
use ct

fn main() {
    ct::deque::new -> d
    d 1 ct::deque::push_back
    d 0 ct::deque::push_front
    d ct::deque::pop_front print nl  // 0
}
```

### pair - Key-Value Pair

```qd
use ct

fn main() {
    "name" "Alice" ct::pair::new -> p
    p ct::pair::key print nl    // name
    p ct::pair::value print nl  // Alice
}
```

## License

MIT
