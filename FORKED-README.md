IrishLAs FORKED version of realexpayments/rxp-hpp-php
=====================================================

Rationale
---------
We intend to use this with Drupal, however we get a dependency conflict when
installing realexpayments/rxp-hpp-php using composer.

- drupal core 8.2.x (and 8.3.x)  requires symfony/validator: ~2.8
  (at least 2.8.0, less than 3.0.0)
- drupal core 8.4.x requires symfony/validator
- realexpayments/rxp-hpp-php requires symfony/validator: 2.7.3
  (exact version)

Solution (our fork)
-------------------
Instead of relying on the upstream realexpayments/rxp-hpp-php, we use our own
fork to get around the dependency conflict.

We've simply REMOVED the dependency on symfony/validator, so we don't get a
complaint about the dependency conflict.

symfony/validator is still installed of course, via Drupal core's dependencies.
