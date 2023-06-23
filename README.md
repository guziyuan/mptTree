# mptTree
MPT 在字典树的基础上做了如下改良：

采用了 Merkle 树的概念，把整棵树的哈希值作为根节点的值，使得每个节点的哈希值只与其自身的值和其子节点的哈希值有关，从而实现了快速验证一个节点的哈希值是否正确，从而防止了数据篡改。

采用了路径压缩，把节点的值和子节点合并为一个节点，从而减少了存储和检索的时间复杂度。

引入了三种节点类型：

a. 叶子节点：存储具体的值，例如以太坊账户的余额和数据。

b. 扩展节点：存储子节点的哈希值。

c. 空节点：表示该节点不存在。

MPT 想要解决的核心问题是以太坊账户数据的存储和检索效率问题。以太坊账户数据是以太坊的核心数据之一，需要高效地存储和检索。传统的字典树虽然可以实现存储和检索，但是存在存储空间浪费和检索效率低下的问题。MPT 通过结合 Merkle 树和路径压缩等技术，优化了存储和检索的效率，提高了以太坊账户数据的处理能力。同时，MPT 的哈希验证机制也确保了数据的安全性和完整性。
