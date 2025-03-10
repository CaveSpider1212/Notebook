---
tags: CPT_S_122
created: 2025-2-19
description: Lesson 6.2
---

### What is a Queue?

- **Queue**: linear data structure with a finite sequence of nodes, where nodes are removed from the front (head) and nodes are inserted at the back (tail)
	- First-in, first-out (FIFO) data structure
	- Considered a restricted or constrained list

### Node Class

##### Header
```
class Node
{
public:
	Node(const string newData = "");
	~Node();
	string getData() const;
	Node* getNextPtr() const;
	void setNextPtr(Node* const newNextPtr);
private:
	string mJob;
	Node* mpNext;
};
```

##### Definition
```
Node::Node(const string newData)
{
    this->mJob = newData;
    this->mpNext = nullptr; // always set the new Node's next pointer to nullptr initially
}

Node::~Node()
{
    cout << "deleting print job: " << this->mJob << endl;
}

string Node::getData() const
{
    return this->mJob;
}

Node* Node::getNextPtr() const
{
    return mpNext;
}

void Node::setNextPtr(Node* const newNextPtr)
{
    this->mpNext = newNextPtr;
}
```

### Queue Class Header

```
class Queue
{
public:
	Queue() { mpHead = mpTail = nullptr; }
	bool enqueue(const string& newData);
	string dequeue();
	bool isEmpty() const;
private:
	Node* mpHead, * mpTail;
};
```

### Initializing a Queue

Done with the `Queue()` constructor
```
Queue::Queue ()
{
	mpHead = mpTail = nullptr;
}
```

### Checking for Empty Queue

```
bool Queue::isEmpty()
{
	return this->mpHead == nullptr && this->mpTail == nullptr
}
```

### Inserting Data into Back of Queue

```
bool Queue::enqueue(const string& newData)
{
	Node* pMem = new Node(newData); // constructor for Node gets called here w/ new
	bool success = false;

	if (pMem != nullptr) {
		// allocated node in heap successfully
		if (this->mpHead == nullptr) {
			// empty queue
			this->mpHead = this->mpTail = pMem;
		}
		else {
			// the queue is not empty
			this->mpTail->setNextPtr(pMem);
			this->mpTail = pMem;
		}

		success = true;
	}

	return success;
}
```

### Removing Data from Front of Queue

```
string Queue::dequeue()
{
	string data = this->mpHead->getData();
	Node* pTemp = this->mpHead; // pTemp refers to the node to delete

	if (this->mpHead == this->mpTail) {
		// one node in queue
		this->mpTail = nullptr;
	}

	this->mpHead = this->mpHead->getNextPtr();

	delete pTemp;
	cout << "finished removing node" << endl;

	return data;
}
```

### Applications

- Operating systems maintain queues of processes that are ready to execute
- Printers queue print requests; first-come, first serve
- Simulations of real world processes, such as movie lines, grocery store lines, etc.