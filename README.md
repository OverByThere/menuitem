# Menuitem

The menuitems API is a simple way to create a menuitem,
which can perform an action when clicked, and display state.

## Example

    exports.main = function(options) {
      // create menuitem for the File menu,
      // and insert it before the 'Quit' menuitem
      require("menuitems").Menuitem({
        id: "myextprefix-some-mi-id",
        menuid: "menu_FilePopup",
        insertbefore: "menu_FileQuitItem",
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
    };
