# Wordpress & Woocommerce Tricks
Simple Function that prevent you using a giant Plugin.
## Displaying Customer IP inside the Woocommerce Order Admin Area
Copy and Paste the code inside functions.php of active theme directory 
```
function order_user_agent( $order ) {
    ?>
	<p class="form-field form-field-wide wc-customer-user">
	    <label>
	        <?php _e( 'User Agent:', 'woocommerce' )?>
	    </label>
	    <?php echo $order->get_customer_user_agent(); ?>
	</p>
	<?php
}
add_action( "woocommerce_admin_order_data_after_order_details", "order_user_agent" );
```
![User Aegent Image](https://drive.google.com/file/d/1vSFNKezxr9vrA39cofebfSRLVBRCtxRA/view?usp=sharing) 
---
*You should Get the output similar to the image*

