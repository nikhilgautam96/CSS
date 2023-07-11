# Display property in CSS :-

-   `display: (inline | block | inline-block | none)` :

    1. `inline` :
        - Takes only the space required by the element.
        - No margin/padding.
        - If we make a block element as inline then it will loose its top and bottom margin and padding.
    2. `block` :
        - Takes full space available in width. So printed in seperate lines.
        - Even if we set the width property to (say 100px), it will srill have margin extended till window end.
        - If we make inline element as block, it take the entire width just like block elements.
    3. `inline-block` :
        - Similar to inline, but we can set margin & padding.
        - We should use this when trying to make a block level element act as inline.
        - It won't take the entire width of spcae available.
    4. `none` :

        - Removes element from document flow.
        - Even the space occuoied by the element is removed and can be used by other elements.

        | display: none                                                                                       | visibility: hidden                                                                                                                                                     |
        | --------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | The `display: none;` property removes the element from the document flow.                           | The `visibility: hidden;` property hides the element but preserves its space.                                                                                          |
        | The element is completely removed from the rendered page, and its space is not reserved.            | The element is still present in the rendered page, but it is not visible.                                                                                              |
        | the element is completely removed from the document flow and the DOM tree.                          | the element remains in the DOM tree.                                                                                                                                   |
        | Any event handlers, styles, or properties associated with the element are effectively disabled.     | The element's contents are not visible but are still present and interactable. Event handlers, styles, or properties associated with the element continue to function. |
        | JavaScript methods like `querySelector` or `getElementById` will not be able to locate the element. | JavaScript methods can locate the element, and its properties can be accessed and modified.                                                                            |
