
# FAQ

## How does it work?

Loqu extracts the metadata for thousands of datasets from the DBNomics project using their API.
Then, we convert it into RDF, which allows it to be loaded into a graph database.
From there, we [infer links](http://dice-group.github.io/LIMES/#/) from the statistical metadata to public knowledge graphs.
This allows us to do cool things like show you the flags of countries by querying Wikidata, and generally augment the  metadata with information from the
outside world.

<!-- Or [FIBO](https://spec.edmcouncil.org/fibo/) [AGROVOC](http://agroportal.lirmm.fr/ontologies/AGROVOC) -->

You can guess the next part: it's the the user interface. We use Vega to build dynamic charts or graphs, and Deck.gl for maps and geographic visualizations.

If you'd like more details on all this, you can [read the paper](https://alexkreidler.github.io/loqu-paper/).

<!-- **Side Note**: I'm planning on also linking to Geonames and LinkedGeoData, and then investigating linking concepts and code list values to ontologies like
FIBO (legal entities/finance), AGROVOC (agriculture), FoodOn (more general food).
There are probably lots of other topics covered in the DBNomics data where there are good ontologies that could be linked to, so suggestions would be welcome. -->

## How can I help?

Well, just by using Loqu you're helping quite a bit. Feel free to share feedback anytime -- it will undoubtedly improve the project.
Also, be sure to submit issues on Github if you run into any bugs.

If you want to contribute data or work on the data pipeline, there is quite a lot to do in the upstream [DBNomics](https://db.nomics.world/) project.

Of course, I'd also appreciate contributors that could work on the UI, data pipeline, or API. 

Others could also get started on documentation, translations, or perhaps more designs/a logo. 


## What's up next?

<!-- We have a public [Roadmap](./roadmap) available. -->

Some of the larger TODOs are as follows, sorted roughly by their priority:

- switch the CSV parser/field inference to Apache Arrow in Rust via WebAssembly (I've already started this) to get better performance on larger files
- improve the visualization editor by integrating a GUI form tool, and allowing users to write JSON-based Vega templates (again, started a while back)
- fetch source data from DBNomics in a tabular format for data-cube visualizations (needs upstream work)
- achieve fuller compliance with the Data Cube and CSVW specs
- allow users to sign in and save visualizations
- investigate GraphQL-LD and rethink the APIs
- switch the hacky geographic visualization code over Deck.gl with Kepler.gl and think about how to expose geographic visualizations to users, perhaps [vega-deck.gl](https://github.com/microsoft/SandDance/tree/master/packages/vega-deck.gl)
- federate metadata as well as data so users could run their own instances of Loqu to create metadata, or use Loqu to visualize data with externally provided metadata

## Who made this?

Alex Kreidler: [website](https://alexkreidler.com/), [Github](https://github.com/alexkreidler). Feel free to reach out on Github or via email at alex@ my domain.

## What's the name?

Loqu is a Greek root that means **to speak**. It is found in some fabulous words like "loquacious" or "eloquent."

I find it particularly apt for technology built on the Semantic Web, which aims to create descriptions of the structure and semantics (meaning) of data with reusable ontologies, and thus perhaps enhance the ability of people to communicate with data.

## What Loqu is Not

Loqu does not aim to be one of the following types of tools:

- ETL
- BI/complex visualization
- Tool for cross-dataset (or graph-wide) queries

If you want one of those, we recommend OpenRefine and Apache Superset.

If you'd like to run queries on the entire dataset, you'd need to export all the data, something that the DBNomics project currently doesn't have good support for.
