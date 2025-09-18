# RichTextExtension

1.Enable Plugin

<img width="1020" height="175" alt="image" src="https://github.com/user-attachments/assets/fee96b62-891f-4346-9603-986bc2a71711" />

2.Hyperlink

Create a blueprint class that inherits from RichHyperLinkDecorator

<img width="571" height="113" alt="image" src="https://github.com/user-attachments/assets/08df23a8-3dd3-4103-bf0c-33ac2ffd3f6e" />

Create a DataTable and select the corresponding structure

<img width="480" height="228" alt="image" src="https://github.com/user-attachments/assets/25361520-c239-4232-bbef-eefc74761c82" />

Open the blueprint class you just created and set the default values

<img width="513" height="266" alt="image" src="https://github.com/user-attachments/assets/bb4577e6-f258-4b70-bbe8-abeb90798739" />

Set the Decorator for rich text

<img width="793" height="462" alt="image" src="https://github.com/user-attachments/assets/cfa40434-aea1-4cdf-bc5f-38a81e3d1843" />


Test case: 

`<a id="Test" href="content" operate="Test">TestClickLink</>`

id: The RowName of your DataTable.

<img width="175" height="45" alt="image" src="https://github.com/user-attachments/assets/755cd0e5-6f5c-497b-9eb3-ef2f613f7d74" />

You can override the OnClickHyperlink event.

<img width="1012" height="434" alt="image" src="https://github.com/user-attachments/assets/271c27fc-68d2-4e67-9b4b-9e8c92251395" />


3.Tooltip/Toptip

The steps are the same as above.
The Decorator classes are RichTooltipDecorator and RichToptipDecorator.

Test case: 
```
<tooltip text="Tooltip infos" id="Test">TestToolTips</>
<toptip text="Toptip Info" id="Test">TestToptip</>
```

<img width="338" height="100" alt="image" src="https://github.com/user-attachments/assets/d1b92448-4f1a-4389-ac1a-38528fad0d49" />

Top Tip:
You need to adjust the Fill Height parameter.

<img width="969" height="27" alt="image" src="https://github.com/user-attachments/assets/4e7c76d3-363e-4eee-8129-cf946cf354f1" />

<img width="340" height="141" alt="image" src="https://github.com/user-attachments/assets/f9730677-2cf1-49d9-b8c2-31f9879ea948" />

<img width="337" height="130" alt="image" src="https://github.com/user-attachments/assets/535ccc5a-dff1-4b8a-8b9e-fba1d3baa0f8" />

4.Play text letter by letter

Create a RichTextAnim object, and call PlayTextAnim.

<img width="1140" height="635" alt="image" src="https://github.com/user-attachments/assets/448cb4c1-04b0-447a-a743-938e56f1d7ca" />

