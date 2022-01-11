# Views Calc Distinct

Views calc doesn't calculate correct values if used in a view with one ore more relationships that will create multiple rows in the result which are limited by a distinct setting. If the query is set to "distinct" the calculation will add the total calculation of all queries even for rows that are hidden by the distinct statement. This behavior in general is correct from a query's point of view, but it will not match the customer's expectation.

This module solves this issue. After installation it will correct all views calc displays out of the box. For finer grained control, you can choose the "views calc distinct" display in a view and set the option "Enable Views Calc Distinct". This will correct the calculation of results with a distinct query for a specific view.

To see an example of what this module is useful for, [take a look at this explanation and snapshots](https://github.com/backdrop-ops/contrib/issues/607#issuecomment-1010126111).

## Known Issues

- Depending on the complexity of the view, some views with relationships may not work.
- Custom fields with multiple value will usually not work. For now, stick to single value fields in custom fields.

## Installation

- Install this module using the [official Backdrop CMS instructions](https://backdropcms.org/guide/modules)

## Dependencies

- [Views Calc](https://www.drupal.org/project/views_calc)

## Current Maintainers

 - [@argiepiano](https://github.com/argiepiano)
 - Collaboration and co-maintainers welcome!

## Credits

 - Ported from Drupal 7 to Backdrop CMS by [@argiepiano](https://github.com/argiepiano)
 - Maintainer on drupal.org: [KarenS](https://www.drupal.org/user/45874)

## License

This project is GPL v2 software. See the LICENSE.txt file in this directory for
complete text.
