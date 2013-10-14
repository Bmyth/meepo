meepo
=====

it is a jQuery plugin to build fancy navigation web element

how to use
-----------
fetch the files: meepo.js and meepo.css, add them in your page(don't forget to add jQuery before that), use it as the example and have fun.

Example
-----------
```javascript
$('.navigation-bar').meepo({
  elements:[
            {
              title:'blog', desc:'here is my blog', frontColor: "#ffffff", backColor: '#B0DCF9', render: renderBlog
            },
            {
              title:'time line', desc:'time line about life', frontColor: "#ffffff", backColor: '#B4D4D4'
            },
            {
              title:'gallary', desc:'my pictures', frontColor: "#ffffff", backColor: '#FACBC0', render: renderGallary
            },
            {
              title:'me', desc:'profile and contact info', frontColor: "#ffffff", backColor: '#E1CFFC'
            }
          ]
});
            
function renderBlog(container){
	return $('<div class="blog">here you can insert the blog body</div>').appendTo(container);
}

function renderGallary(container){
	return $('.element-template .gallary').clone().appendTo(container);
}

```

bind the element you want to render as the navigation element, pass the elements params to render each unit. 
You can just set the title, description and color, or customised render funtion for shelf part and grand part (see the option list).
Also you can do a lot of things of style to make your page fancy.

demo
-----------
you can visit my blog to see what it looks like: http://xy01.ap01.aws.af.cm

options
-----------
### Options ###

<table class="table table-bordered table-striped">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Default</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>size</td>
			<td>number</td>
			<td>600</td>
			<td>the width of the navigation bar</td>
		</tr>
		<tr>
			<td>shelfOffset</td>
			<td>number</td>
			<td>300</td>
			<td>the vertiacal offset of the navigation bar</td>
		</tr>
		<tr>
			<td>elementSmallSize</td>
			<td>number</td>
			<td>40</td>
			<td>the height of element when the shelf goes up</td>
		</tr>
		<tr>
			<td>grandHeight</td>
			<td>boolean</td>
			<td>equals to the size</td>
			<td>basic height to render the element in grand part(the detail view)</td>
		</tr>
		<tr>
			<td>homeFrontColor</td>
			<td>string</td>
			<td>"#ffffff"</td>
			<td>front color of the home element</td>
		</tr>
		<tr>
			<td>homeBackColor</td>
			<td>string</td>
			<td>"#cccccc"</td>
			<td>back color of the home element</td>
		</tr>
		<tr>
			<td>elements[idx].title</td>
			<td>string</td>
			<td>element title</td>
			<td>element title</td>
		</tr>
		<tr>
			<td>elements[idx].desc</td>
			<td>string</td>
			<td>element description</td>
			<td>to render element description when hover on</td>
		</tr>
		<tr>
			<td>elements[idx].frontColor</td>
			<td>string</td>
			<td>"#ffffff"</td>
			<td>element front color to render text</td>
		</tr>
		<tr>
			<td>elements[idx].backColor</td>
			<td>string</td>
			<td>"#cccccc"</td>
			<td>element back color to render pure background</td>
		</tr>
		<tr>
			<td>elements[idx].shelfElement</td>
			<td>string</td>
			<td></td>
			<td>the dom string for jQuert to render element in shelf</td>
		</tr>
		<tr>
			<td>elements[idx].renderShelf</td>
			<td>function</td>
			<td></td>
			<td>function for element to render in shelf, need accept container inside to appendTo</td>
		</tr>
		<tr>
			<td>elements[idx].grandElement</td>
			<td>string</td>
			<td></td>
			<td>the dom string for jQuert to render element in grand (the detail view when selected)</td>
		</tr>
		<tr>
			<td>elements[idx].render</td>
			<td>function</td>
			<td></td>
			<td>function for element to render itself in grand part, need accept container inside to appendTo</td>
		</tr>
	</tbody>
</table>


