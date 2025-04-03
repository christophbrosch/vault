The Global Product Classification (GPC) is a system developed by GS1 to standardize the classification of products, facilitating global commerce by enabling consistent and accurate communication across different industries and countries. It assigns a unique code to each product category, ensuring that similar products are grouped together in a logical hierarchy. This helps businesses streamline supply chain processes, improve product data management, and enhance searchability and comparison on e-commerce platforms. By adopting GPC, companies can achieve greater efficiency and interoperability in the global market.

The GPC system consists of multiple levels, namely, from top-to-bottom: Segment, Family, Class and Brick. Each becoming more and more fine-grained. The plot below gives an overview on the amount of unique codes associated with each level. During our research we primarily focus on products belonging to the segment "Food / Beverage" which are shown separately in the plot.

[@]
# Distribution
## Segment, Family, Class & Brick

![[gpc_codes_distribution.png]]

## Attributes & Values

According to [@luoAliCoCoAlibabaEcommerce2020] GPC can be classified as a CPV (Category-Property-Value) taxonomy. Implying that the lowest classification level (Brick) has so-called property nodes associated with them. These property nodes in turn have values (list of all possible values for the property) attached to them.  

<mark style="background-color: #ffd400">Quote</mark>
> The taxonomy to organize items in Alibaba (actually almost every e-commerce platforms) is generally based on CPV (Category-Property-Value): thousands of categories form a hierarchical structure according to different granularity, and properties such as color and size are defined upon each leaf node.

In the case of GPC, these property nodes are called Attributes and values, well, values. The following is an example of a Attribute/Value pair for the Brick "Beer":

```json
{
	"brick_code":10000159,
	"brick_title":"Beer",
	"brick_includes":"Includes any products that can be described/observed as a beer made by the fermentation of cereals, usually barley or hops but also maize, wheat, rice and sorghum, by the addition of yeast and water. These products are differentiated by various brewing techniques and include products described as lager, bitter, ale, stout, lambic and specialty beers.Includes beer mixed drinks. ",
	"brick_excludes":"Specifically excludes non-alcoholic beer. Excludes products such as Soft drinks that may be labelled as beer, such as Ginger Beer/Ale and Root Beer."
}
```

Brick 10000159  has 10 Attributes associated with it, one of which is Attribute 20002973:

```json
{
	"attribute_code":20002973,
	"attribute_title":"Taste",
	"attribute_definition":"Indicates, with reference to the product branding, labelling or packaging the descriptive term that is used by the product manufacturer to identify the taste of the beer.",
	"attribute_values": [
	{
		"value_code":30017085,
		"value_title":"BITTER",
		"value_definition":null
	},{
		"value_code":30015674,
		"value_title":"MILD",
		"value_definition":null
	},{
		"value_code":30002515,
		"value_title":"UNCLASSIFIED",
		"value_definition":"This term is used to describe those product attributes that are unable to be classified within their specific market; e.g. goat\'s cheese - goat\'s cheeses is often generically labelled and cannot be further classified."
	},{
		"value_code":30002518,
		"value_title":"UNIDENTIFIED",
		"value_definition":"This term is used to describe those product attributes that are unidentifiable given existing or available product information."
	}]
}
```

Compared to Classification Codes (Segment, Family, Class & Brick), the Attribute-Value Codes don't have to be unique to one leaf node (Brick). In total there are unique 2065 Attributes. 

![[gpc_codes_and_attributes_distribution.png]]

Attributes are not necessarily unique to a BrickCode. On average, a Brick in Segment "Food" has on average 4.55 Attributes associated with it. Compared to the global average 1.37.  

![/home/cbrosch/Repositories/gpc-explorer/plots/distribution_of_number_of_attribues_per_brick.png](file:///home/cbrosch/Repositories/gpc-explorer/plots/distribution_of_number_of_attribues_per_brick.png)

# Task

Given the complexity of the classification system, we have witnessed ourselves how frustrating and time consuming the task of manual classification according to GPC is (see [[14 Labeling]] for examples). Therefore we made it our goal to support manual efforts by providing automated values on brick level. Either a Top-1 or Top-3 result, depending on the accuracy of the system.

# Previous work

We investigated different approaches for classifying products according to gpc in the past. Our first approach was conducted during the masters thesis of Sebastian Bast [[@bast_2023]] in which we used 36.524 products provided to us by Globus. These products were classified according to the brick level.

>Our experiments are based on 36,624 product data records with corresponding product images provided by a German retailer. The dataset contains 69,256 product images and is denoted as dataset A. This dataset, which was used in [1], was extended by 34,518 images obtained through web crawling. The resulting dataset contains 103.774 product images and is denoted as dataset B.

Furthermore this dataset was extended by searching the product name in google and downloading the nth's first hits under the images tab. These images were manually checked.

The results of this work was very promising achieving an F1-score of  0.917 on brick level and 0.931 on class level.

> ![[image-18-x131-y216.png]]

One problem of this work is the requirement of pre-classified data. Bast showed in his master thesis that this system requirements at least X data points:

![[Pasted image 20250403151322.png]]