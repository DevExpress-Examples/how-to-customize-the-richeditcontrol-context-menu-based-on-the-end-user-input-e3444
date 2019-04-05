<!-- default file list -->
*Files to look at*:

* [MainPage.xaml](./CS/MainPage.xaml) (VB: [MainPage.xaml](./VB/MainPage.xaml))
* [MainPage.xaml.cs](./CS/MainPage.xaml.cs) (VB: [MainPage.xaml.vb](./VB/MainPage.xaml.vb))
<!-- default file list end -->
# How to customize the RichEditControl context menu based on the end-user input


<p>This example illustrates how to customize the RichEditControl context menu based on the end-user input. The main idea of this functionality implementation is to handle the <a href="http://documentation.devexpress.com/#Silverlight/DevExpressXpfRichEditRichEditControl_ContentChangedtopic"><u>RichEditControl.ContentChanged Event</u></a> and analyze characters displayed nearby the caret. The following <a href="http://documentation.devexpress.com/#Silverlight/clsDevExpressXtraRichEditAPINativeDocumenttopic"><u>Document Interface</u></a> members are used for this purpose:</p><p><a href="http://documentation.devexpress.com/#CoreLibraries/DevExpressXtraRichEditAPINativeSubDocument_GetTexttopic878"><u>SubDocument.GetText Method</u></a><br />
<a href="http://documentation.devexpress.com/#CoreLibraries/DevExpressXtraRichEditAPINativeDocument_CaretPositiontopic"><u>Document.CaretPosition Property</u></a></p><p>Then the <a href="http://documentation.devexpress.com/#Silverlight/DevExpressXpfRichEditRichEditControl_GetBoundsFromPositiontopic"><u>RichEditControl.GetBoundsFromPosition Method</u></a> is called to obtain a location where the context menu should be invoked. Take special note of the way a <a href="http://documentation.devexpress.com/#Silverlight/clsDevExpressXpfRichEditRichEditControltopic"><u>RichEditControl Class</u></a> descendant is created  with the <strong>ShowMenu</strong> method, which allows you to invoke the menu programmatically. When the menu is invoked, the <a href="http://documentation.devexpress.com/#Silverlight/DevExpressXpfRichEditRichEditControl_PopupMenuShowingtopic"><u>RichEditControl.PopupMenuShowing Event</u></a> is raised, which allows you to customize the menu items.</p>

<br/>


