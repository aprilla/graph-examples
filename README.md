# graph-examples

The intent is to provide more complete and extensive examples than what is reasonable to include in DataStax documentation or blogposts.  This will include DataStax Graph Loader mapping scripts, schemas, example traversals, things to try in DataStax Studio, and application code examples.  Feel free to use and modify any of these for your own purposes.  There is no warranty or implied official support, but hopefully the examples will be useful as a starting point to show various ways of loading and experimenting with graph data.  And if you see anything that could be improved or added, issue reports and pull requests are always welcome!

Download DSE (includes DSE Graph), DataStax Studio, and the DSE Graph Loader at https://academy.datastax.com/downloads.

## Graph Resources:

### Documentation
- Apache TinkerPop [documentation](http://tinkerpop.apache.org/docs/current/reference/), [getting started tutorial](http://tinkerpop.apache.org/docs/current/tutorials/getting-started/), and [common recipes](http://tinkerpop.apache.org/docs/current/recipes/)
- DataStax Enterprise Graph [documentation](http://docs.datastax.com/en/dse/5.1/dse-dev/datastax_enterprise/graph/graphTOC.html)
- [sql2gremlin.com](http://sql2gremlin.com) - to help migrate from sql to graph, used in the [Northwind](/northwind) graph example

### Video tutorials

- DataStax Academy [DSA 330 course](https://academy.datastax.com/resources/ds330-datastax-enterprise-graph) on DSE Graph, a self-paced course covering both DSE Graph and Gremlin as a traversal language.
- DataStax Academy Gremlin Recipes
  - [Gremlin as a stream](https://vimeo.com/user35188327/review/215965720/22e5289c7e)
  - [SQL to Gremlin](https://vimeo.com/user35188327/review/215966324/84ecf9b4ee)
  - [Recommendation engine with Gremlin](https://vimeo.com/user35188327/review/216119433/0dcc2e6055)
  - [Recursive traversal](https://vimeo.com/user35188327/review/216179907/b40808f0a2)
  - [Path with Gremlin](https://vimeo.com/user35188327/review/216259582/8ae9955826)

### Blog posts

- [Getting started with the DataStax Graph Loader](http://www.datastax.com/dev/blog/dgl-basics)
- [Gremlin's Time Machine](https://www.datastax.com/dev/blog/gremlins-time-machine) - a post about how to use the TinkerPop SubgraphStrategy to traverse your graph at a specific version or time in its history.
- [graphoendodonticology](https://www.datastax.com/2017/03/graphoendodonticology) - a resource to troubleshoot your graph
- [Reducing Computational Complexity with Correlate Traversals](https://www.datastax.com/2017/04/reducing-computational-complexity-with-correlate-traversals) - a post about calculating network centrality in various manners and the associated cost.
- [Introducing DSE Graph Frames](http://www.datastax.com/dev/blog/dse-graph-frame) - how to use DSE Graph with Spark's GraphFrames with the associated [DseGraphFrames example](/dse-graph-frame)
- [Learn How to Build a Domain Specific Language with DSE Graph](https://www.datastax.com/dev/blog/gremlin-dsls-in-java-with-dse-graph)
- Large graph loading best practices, [part 1](http://www.datastax.com/dev/blog/large-graph-loading-best-practices-strategies-part-1) and [part 2](http://www.datastax.com/dev/blog/large-graph-loading-tactics-part-2)
- Blog series from [DuyHai Doan](https://twitter.com/doanduyhai)'s blog:
  1. [Gremlin as a Stream](http://www.doanduyhai.com/blog/?p=13224)
  2. [SQL to Gremlin](http://www.doanduyhai.com/blog/?p=13260)
  3. [Recommendation Engine Traversal](http://www.doanduyhai.com/blog/?p=13285)
  4. [Recursive Traversals](http://www.doanduyhai.com/blog/?p=13301)
  5. [Path Object](http://www.doanduyhai.com/blog/?p=13320)
  6. [Projection and Selection](http://www.doanduyhai.com/blog/?p=13352)
  7. [Variable Handling](http://www.doanduyhai.com/blog/?p=13374)
  8. [The `sack()` Operator](http://www.doanduyhai.com/blog/?p=13404)

### Presentations

- [The Gremlin Graph Traversal Language](https://www.slideshare.net/slidarko/the-gremlin-traversal-language), a presentation by Marko Rodriguez and Daniel Kuppitz
- Fighting Fraud with Graph Databases Webinar [recording](https://www.youtube.com/watch?v=H5MmSL1c9Zs) and [slides](https://www.slideshare.net/DataStax/webinar-fighting-fraud-with-graph-databases).  Presented by DataStax and Cambridge Intelligence.

### Help!

- [DataStax support portal](https://support.datastax.com) (for current DataStax customers)
- [DataStax Academy Slack](https://academy.datastax.com/slack) in the dse-graph channel
- [Gremlin-users google group](https://groups.google.com/forum/#!forum/gremlin-users)
- Stack overflow with the [datastax-enterprise/datastax-enterprise-graph](http://stackoverflow.com/questions/tagged/datastax-enterprise+datastax-enterprise-graph) tag

### Graph language drivers
- Apache TinkerPop [Gremlin Language Variants](http://tinkerpop.apache.org/docs/current/tutorials/gremlin-language-variants/) - describes TinkerPop's idiomatic language support in the form of a fluent API
- [Introduction to DataStax Driver Usage of Gremlin Language Variants](http://www.datastax.com/dev/blog/datastax-drivers-fluent-apis-for-dse-graph-are-out)
- [Java](http://docs.datastax.com/en/developer/java-driver-dse/1.4/) - includes both a String based and fluent API
- [Python](http://docs.datastax.com/en/developer/python-dse-driver/2.2/ - includes both a String based and fluent API 
- [Node.js](http://docs.datastax.com/en/developer/nodejs-driver-dse/1.3/)
- [C#](http://docs.datastax.com/en/developer/csharp-driver-dse/2.0/)
- [C/C++](http://docs.datastax.com/en/developer/cpp-driver-dse/1.2/)
- [Ruby](http://docs.datastax.com/en/developer/ruby-driver-dse/2.0/)
- [PHP](http://docs.datastax.com/en/developer/php-driver-dse/1.1/)
- Looking for Scala? Take a look at [this example](https://github.com/mpollmeier/gremlin-scala-examples/tree/master/dse-graph) of using Scala with the DataStax Java driver

### Additional datasets

For additional interesting datasets, you might consider the following resources:

- [Stanford Large Network Dataset Collection](https://snap.stanford.edu/data/) - a collection of connected data in various categories such as social data, web graphs, product co-purchasing networks, review data, etc.
- [Awesome Public Datasets](https://github.com/caesar0301/awesome-public-datasets) - a github repository with links to collections, large and small, of interesting public data.  These are further categorized by industry and data type such as energy, government, machine learning, time series, sports data, transportation, etc.
- [CRAWDAD](http://crawdad.org/) - the Community Resource for Archiving Wireless Data At Dartmouth.  This includes wireless network trace data from a variety of sources.