# ALEXANDER NAIDEN

## PERSONAL INFORMATION
|                   |                                             |
|-------------------|---------------------------------------------|
|**Address:**       |Karl Liebknecht str., 220036 Minsk, Belarus  |
|**Telephone:**     |+375 29 859 67 56                            |
|**Email:**         |naidenav@gmail.com                           |
|**Date of bigth:** |15th April 1994                              |
|**Marital status:**|single                                       |

## OBJECTIVE
I am seeking a position with a company where i can realize my intellectual and physical capabilities. I am used to learning and adapting to something new. In programming, I am attracted to solving complex problems and the need to use creativity and ingenuity.

## SKILLS
- HTML
- CSS
- JavaScript
- Git

For half a year before the rs-school course I studied html, css, javascript, node js and created my own website about cooking.

## SAMPLE CODE
```javascript
$(document).ready(function(){
	$('.menu-btn').click(function(event){
		event.preventDefault();
		$('.menu').toggleClass('menu-active');
		$('.content').toggleClass('content-active');
		$('.menu-btn').toggleClass('menu-btn-active');
	});
});

function  displayCategory() {
	$.getJSON("categories.json", function(data_1) {
		let  dataCategories = data_1;
		let  output = "<div id=block-icon>";
		for (let  i  in  dataCategories) {
			output += "<div><a href='#' id=category-" + i + "><figure class='categories-icon'><img src='" + dataCategories[i].icon + "' width=100px height=100px><figcaption>" + dataCategories[i].name + "</figcaption></figure></a></div>";
		};
		output += "</div>"
		document.getElementById("catList").innerHTML=output; 
		$.getJSON("recipes.json", function(data_2) {
			let  dataRecipes = data_2;
			for (let  i  in  dataCategories) {
				$(`#category-${i}`).click(function(event) {
					event.preventDefault();
					output = "<ol>";
					for (let  j  in  dataRecipes) {
						if (dataRecipes[j].catId == i) {
						output += "<li><a href='recipe.html?number-recipe=" + j + "' id=recipe-" + j + ">" + dataRecipes[j].recipename + "</a>";
						};
					};
					output += "</ol>";
					document.getElementById(`catList`).innerHTML=output;
				});
			};
		});
	});
};

window.onload = displayCategory;
```
## WORK EXPERIENCE

## EDUCATION
- **Belarussian National Technical University**
Civil Engineering faculty, Industrial and civil Engineering (2011 - 2016)

## ENGLISH
- A2 - Pre-Intermediate