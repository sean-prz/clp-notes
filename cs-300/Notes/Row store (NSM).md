_Also called N-ary storage model_-

## Fixed vs Variable Length

### **Fixed length**
Finding a field is done via a simple calculation.
### **Variable length**
Finding a field is done via a pointer.
Attributes are represented by (offset, length) pairs, and actual data is stored after all fixed length fields.
**Slotted page**
A page with a header that contains the number of record, the end of free space and location and size of each record.

![[Pasted image 20250303153811.png | 300  ]]





-- -
## Pros and Cons

**Advantages**
- Good (OLTP) entire tuple queries
- Fast insert, update, deletes.
**Disadvantages**
- Slow for large queries, subset and aggregation queries
