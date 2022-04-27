## MIMOS

The MIMOS project aims at developing methods and tools to enable deterministic modeling of real-time systems with predictable timing behaviors, and also  supporting incremental updates after deployment without redesigning the whole system.

### Publications
Here we list the related publications.

- Wang Yi, Morteza Mohaqeqi, Susanne Graf, **A Deterministic Model for the Design and Update of Real-Time**, 2020.


### Tools
Here goes a list of developed [tools](https://user.it.uu.se/~mormo492/datoor/datoor.htm)


### Examples

This is simple example.

```markdown
process f(int out V) {
    Repeat {
        write 1 on V;	 
    }
}
process g(int in U; int threshold; int out V) {
    int count = 0;       // local variable
        Repeat {
            read(U);	// read from a channel
                count = count + 1;
                if count == threshold  
                    write 1 on V; 		// write to a channel
                    count = 0;	
        }
}
int channel X, Y;
f(X) || g(X, 5, Y);    // concurrent execution
```

### Contact

Uppsala University
