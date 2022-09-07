# MongoDB

Foobar is a Python library for dealing with word pluralization.

## Why MongoDB
- It is schema-free and does away with the need to define a fixed structure. You can just start adding data and it isn’t necessary to have any relation between those. The only restriction with this is the supported data structures.

- The document format used in place of rows and columns can be easily mapped by programming languages

- Horizontally scalable i.e, data can be distributed across multiple servers to improve performance whereas for relational databases, performance can only be improved by increasing the performance of the server it’s run on.

- Provides good support for Hierarchical data like JSON or XML. For large amounts of unstructured data, SQL based DB would be significantly slower.

- Offers higher efficiency and reliability which in turn helps with better storage capacity and speed requirements.

## Example

```
{

   "coord":{

      "lon":-0.13,

      "lat":51.51

   },

   "weather":[

      {

         "id":300,

         "main":"Drizzle",

         "description":"light intensity drizzle",

         "icon":"09d"

      }

   ],

   "base":"stations",

   "main":{

      "temp":280.32,

      "pressure":1012,

      "humidity":81,

      "temp_min":279.15,

      "temp_max":281.15

   },

   "visibility":10000,

   "wind":{

      "speed":4.1,

      "deg":80

   },

   "clouds":{

      "all":90

   },

   "dt":1485789600,

   "sys":{

      "type":1,

      "id":5091,

      "message":0.0103,

      "country":"GB",

      "sunrise":1485762037,

      "sunset":1485794875

   },

   "id":2643743,

   "name":"London",

   "cod":200

}
```

## Point to Note
These tables will be required - Coordinates, Weather, Main, Wind, Clouds, Sys and one parent table which has foreign key relationship to all these other tables.


So, we need to come up with the tables to be used, set data types for all the attributes, define the relationships, and create all these tables before going ahead and adding data to these tables. This is termed as having a "fixed schema" as the structure is defined before adding data.


MongoDB uses dynamic schema and inherently supports hierarchical data (nested data) as it’s a NoSQL database. This means that the schema (structure) is dynamically created from the data and individual data entries don't have to be in the same format. Hence, there’s no overhead to adding complex data like we saw above, making it a preferred choice to store this kind of data.

## Advantage of MongoDB
As MongoDB can be scaled horizontally, MongoDB clusters can be geographically distributed on servers to improve query performance.


MongoDB is a persistent (or disk-based) database unlike Redis, which is a NoSQL based in-memory database. Though Redis can be significantly faster than MongoDB when the stored data is smaller in size, MongoDB can operate much faster as the database gets larger.

***Sharding***  is the concept of storing partitions of data (shard) in different database servers.

- For sharding in relational databases like MySQL, application level changes are required as well as needing to suffer downtime due to interlinking of the tables. These also require servers with high specifications which are costly.

- Due to the horizontal scalability, sharding in MongoDB is cost-effective as buying several low-cost machines is often cheaper than buying a smaller number of machines with significantly higher specifications.

Additionally, MongoDB stores data in the BSON (Binary JSON) format.

- BSON basically is an improvised version of the popular JSON format used

- BSON supports additional data types like Date out of the box in addition to the data types like String, Boolean, Number, Array supported by JSON.

- Parsing data is much quicker with BSON as data isn’t saved in text form (human-readable) as in JSON. BSON adds metadata to like lengths of string used to make queries faster

- As popular programming languages like JavaScript, Python has data types (JavaScript Object, Python Dictionary) to which JSON can be directly mapped, it removes any transformation required to process the data.

## Author
@Kanishk Mahor
