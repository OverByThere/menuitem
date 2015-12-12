# Menuitem

Provides an API to create menuitems using the addon-sdk. Compared to the base
version, this supports separators around the item.

## Example

    // create menuitem for the File menu,
    // and insert it before the 'Quit' menuitem
    require("menuitem").Menuitem({
      id: "myextprefix-some-mi-id",
      menuid: "menu_FilePopup",
      insertbefore: "menu_FileQuitItem",
      separatorbefore: true,
      separatorafter: false,
      "label": _("label"),
      "accesskey": _("label.ak"),
      image: self.data.url("icon.png"),
      className: 'pizazz',
      disabled: false,
      checked: false,
      onCommand: function() {
        // do something
      }
    });
