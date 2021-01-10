Toolbar positions are correctly persisted, but incorrectly restored.

1. Run the app, align both toolbars to the left one under another.
2. Stop the app.
3. Open the user.config file, located somethere at C:\Users\<user>\AppData\Local\ToolstripLoad\ToolstripLoad_Url_<random string>\1.0.0.0, check that both toolbars' locations are like this:
```xml
        <System.Windows.Forms.ToolStripSettings.toolsettings.ToolStripFilters>
            <setting name="Name" serializeAs="String">
                <value>ToolStripFilters</value>
            </setting>
            <setting name="Location" serializeAs="String">
                <value>7, 25</value>
            </setting>
        </System.Windows.Forms.ToolStripSettings.toolsettings.ToolStripFilters>
        <System.Windows.Forms.ToolStripSettings.toolsettings.ToolStripMain>
            <setting name="Name" serializeAs="String">
                <value>ToolStripMain</value>
            </setting>
            <setting name="Location" serializeAs="String">
                <value>7, 0</value>
            </setting>
        </System.Windows.Forms.ToolStripSettings.toolsettings.ToolStripMain>
```
4. Run the app again and observe the bottom toolbar shifted by few pixels to the right.
5. Close the app and see that the location value for `ToolStripFilters` has changed.