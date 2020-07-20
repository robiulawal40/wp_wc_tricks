# Wordpress & Woocommerce Tricks
Simple Function that prevent you using a giant Plugin
## Displaying Customer IP inside the Woocommerce Order Admin Area
`add_action( 'woocommerce_checkout_update_order_meta', 'wc_store_user_ip' ); function wc_store_user_ip( $order_id ) { update_post_meta( $order_id, 'Customer IP', $_SERVER['REMOTE_ADDR'] ); }`
