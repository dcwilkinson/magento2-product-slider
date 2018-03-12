# Magento 2 Product Slider

Displays a slider of products assigned to a category. 

The <code>getProducts</code> method accepts one argument - a category ID. It retrieves the collection of all products within that category, assuming they are enabled and they are set to display singularly.

Within the template file, we pass the ID of the category to a method call on the block object:

    $categoryprods = $block->getProducts(3);

We then loop through each iteration and display product data as required.

I'm using slick slider to display the products in a nice, simple carousel. The full configuration and documentation is available here: http://kenwheeler.github.io/slick/

To render this on the frontend, you can add the following in the CMS content edit area: 

    {{block class="Dcwilkinson\ProductSlider\Block\ProductSlider" template="Dcwilkinson_ProductSlider::product_slider.phtml"}}

Alternatively, you can add via XML:

    <referenceContainer name="content">
	    <block class="Dcwilkinson\ProductSlider\Block\ProductSlider" name="productslider" template="Dcwilkinson_ProductSlider::product_slider.phtml" before="-"/>
    </referenceContainer>
