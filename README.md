# Assignment

## Workflow

* Search for products based upon a user-provided search string
* Use the first item in the search response as input for a product recommendation search
* Retrieve reviews of the first 10 product recommendations
* Rank order the recommended products based upon the review sentiments

## Solution details

This solution consists of a Web application developed using `JSF Framework` to consume Walmart's API which can search for a product and rank its recommendation based on ratings/reviews. The search results can be filtered using two options given below. 
* Best Sellers
* Increasing price
 
Default search action is without filters. 

### Assumptions:
* Products with *no reviews* are assumed to have an `Average overall rating: 0.0`

## Testing

Solution is deployed in AWS 

http://ec2-52-35-123-130.us-west-2.compute.amazonaws.com/walmart_assignment/faces/Search.xhtml



## Environment

* AWS EC2 bitnami tomcat
* JSF 2.2, Tomcat 7.0
* specify apiKey and api url in  WebContent/WEB-INF/config.properties

```
apiKey=xxxx
api_url=http://api.walmartlabs.com/v1/
```

## Deployment
* Deploy `walmart_assignment.war` available from `installation` directory to `Tomcat` server's `webapps` directory
* Update `config.properties` with `api_url` and `api_key`
