# Jupyter Notebooks

Archive of materials from UC Berkeley's MOOC on Spark.

- **Intro** shows basic syntax.
- **Analysis** has 3 end-to-end projects.


The tutorial from UCB is missing key steps right at the start. It does not show how to create the sqlContext

from pyspark import SparkContext
from pyspark.sql import SQLContext

# Only one context is allowed, and is automatically created
sc = SparkContext.getOrCreate()

# Note that this does not create a HiveContext, as the ucb tutorial specifies
sqlContext = SQLContext(sc)

