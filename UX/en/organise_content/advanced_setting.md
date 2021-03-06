# Advanced settings : metadata

You can modify a document's behavior or associated actions using specific parameters described in a file named `_meta.txt`.

To modify the behavior of a folder in the application, the meta file must be placed inside the targeted folder, and named `_meta.txt`.

To modify the behavior of a document in the application, the meta file must be named after the document's file name followed by the suffix `_meta` and the `txt` extension. It must be saved at the same location as the target document. 

> Example: for a file named `1 - image.jpg`, the corresponding meta file should to be named as follows : `1 - image_meta.txt`.

In the meta file, each line (called `meta`) shall describe a parameter using the following structure: `metaName = value`

A binary meta (true or false) is described as follows:  `metaName = true`. It's default value is `false`. The values `1` (true) and `0` (false) can also be used.

To apply a specific behavior to a set of documents, use the `*.` prefix on the description of the meta and save the meta file in the folder containing the set of targeted documents

> Example : `*.table.hideCommands = true`

## Value types

|Type         | Description | Examples|
|:------------|:------------|:--------|
| `text`      | a string of characters | `some text`, `My document` |
| `number`    | an integral or decimal number | `123`, `123.45` |
| `dimension` | a size in pixels or a percentage of the containing view | `400`, `75%` |
| `boolean`   | true or false | `true`/`false`, `1`/`0`  |


## Metadata supported

| Metadata Key                      | Type         | Default | Description |
|:--------------------------------- |:-------------|:--------|:-|
| `desiredHeight`                   | `dimension`  | 400     | sets the default height of the document |
| `desiredWidth`                    | `dimension`  | 400     | sets the default width of the document |
| `isPaper`                         | `boolean`    | false   | removes the background of the document's buttons (action and close buttons)|
| `maxHeight`                       | `dimension`  | -       | sets the maximum height |
| `maxWidth`                        | `dimension`  | -       | sets the maximum width |
| `minHeight`                       | `dimension`  | -       | sets the minimum height |
| `minWidth`                        | `dimension`  | -       | sets the minimum width |
| `name`                            | `text`       | file name | change the displayed name of the document to "A name" (example) |
| `orientation`                     | `number`     | 0       | rotates the document: `-90` to turn left, `90` to turn right or `180` to flip the document |
| `table.hideCommands`              | `boolean`    | false   | hides the control buttons of a document (previous/next page, video playback controls…) |
| `table.noRotate`                  | `boolean`    | false   | inhibits rotation for the document |
| `table.viewer`                    | `cdux`       | unset   | Makes sure the `cdurl` link will be displayed inside Compositeur Digital UX |
                                 


<!--| `table.noScale` | " | inhibits resizing for the document |-->
<!--| `table.noMove` | " | inhibits moving the document | -->

## Content specific metadata

### Video

| Metadata Key                      | Type      | Default | Description |
|:--------------------------------- |:----------|:--------|:-|
| `video.autoplay`                  | `boolean` | true    | start playing video on display |
| `video.autoplay.delay`            | `number ` | 0       | delay autoplay by the number of seconds specified |
| `video.rewind`                    | `boolean` | false   | go back to the first frame when the video ends |
| `video.loop`                      | `boolean` | false   | replay from start when the video ends |
| `video.controls.alwaysvisible`    | `boolean` | false   | force the display of the video playback controls |

### Web

| Metadata Key                      | Type      | Default | Description |
|:--------------------------------- |:----------|:--------|:-|
| `web.manipulationMode`            | `number`  | 0       | If `1`, the user will have to enable navigation mode, then the view will behave like a browser. If `0`, the navigation mode will be reduced. |
| `web.showChrome`                  | `boolean` | false   | display a navigation bar at the top of the view |
| `web.viewport.width`              | `number`  | 1000    | Sets the default width of the page view |
| `web.viewport.height`             | `number`  | 800     | Sets the default height of the page view |

### Loan simulator

| Metadata Key                      | Type     | Default | Description |
|:--------------------------------- |:---------|:--------|:-|
| `simulator.creditMaxValue`        | `number` | 800000  | sets the maximum value of a loan |
| `simulator.creditTickFrequency`   | `number` | 5000    | sets the interval between two values for a loan |
| `simulator.creditDefaultValue`    | `number` | 300000  | sets the default loan value |
| `simulator.durationMinValue`      | `number` | 5       | sets the shortest duration of a loan |
| `simulator.durationMaxValue`      | `number` | 30      | sets the longest duration of a loan |
| `simulator.durationTickFrequency` | `number` | 1       | sets the interval between two values for a loan duration |
| `simulator.durationDefaultValue`  | `number` | 20      | sets the default duration of a loan |






[Back to Organise Content](index.md)
