1. In Scala, arrays are zero based, and you can access an element by specifying  index in parentheses. So the first element in a Scala array named arg is arg\(0\), not arg\[0\], as in Java.
2. Scala Array and List are 0 based index.
3. Scala tuples have 1 based index to access elements in tuple. 
4. if code contains any _vars \_it is imperative style. if code contains no_ var,\_ mean all \_val, \_it is functional style. So when programing in scala try to be using no var. As function programming helps you to write more understandable, less error prone code in fewer line . 
5. A balanced attitude for Scala programmers  :Prefer vals, immutable objects, and methods without side effects.
   Reach for them first. Use vars, mutable objects, and methods with side  effects when you have a specific need and justification for them.
6. A literal identifier is an arbitrary string enclosed in back ticks \(\` . . . \`\).    Some examples of literal identifiers are:
   \`x\` \`&lt;clinit&gt;\` \`yield\`. You cannot write Thread.yield\(\) because yield is    a reserved word in Scala. However, you can still name the method in back    ticks, e.g., Thread.\`yield\`\(\).



