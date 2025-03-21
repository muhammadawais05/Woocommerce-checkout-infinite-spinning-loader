# Woocommerce-checkout-infinite-spinning-loader
Here are some steps you can follow to fix the issue:

0. Clear all server-side and browser cache, and enable development mode (if available with the site’s host)
1. Temporarily switch your theme to Storefront or Twenty Twenty theme.
2. Try to reproduce the problem: Check whether you still encounter the issue!

If the problem is resolved, it’s a theme conflict. If not, continue to the next steps.

3. Temporarily deactivate all plugins except WooCommerce. You can do this manually or use a plugin to help (see below for tools).
4. Try to reproduce the problem again. If the problem is resolved, it’s a plugin conflict. To figure out which plugin is causing the problem, continue to the next step.
5. Reactivate your other plugins one by one, testing after each, until you find the one causing conflict.
6. If the spinning loader persists, try adding this CSS under Appearance → Customize → Additional CSS:
  .woocommerce .blockUI.blockOverlay {
      position: relative!important;
      display: none!important;
    }
