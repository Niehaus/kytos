**k-action-menu**

================= ====== =========================================== 
name              type   description                                 
================= ====== =========================================== 
addActionMenuItem object Add a new action item in the k-action-menu. 
================= ====== =========================================== 

**k-info-panel**

============= ====== =========================================== 
name          type   description                                 
============= ====== =========================================== 
showInfoPanel Object Show the info panel in the right.           
hideInfoPanel NULL   Hide the info panel displayed in the right. 
============= ====== =========================================== 

The `k-info-panel` can be triggered by a `k-button` or a `k-action-menu` or
anything that calls the method created to set-up a new `k-info-panel`.

**Example**

.. code-block:: html

    <template>
        ...
    </template>

    <script>
    /* All the javascript methods are optional */
    module.exports = {
        methods: {
            showInfoPanel()  {
                var content = {
                    "component": 'search-hosts',
                    "content": {}, /* Content used in the component */
                    "icon": "search",
                    "title": "Search Hosts",
                    "subtitle": "by kytos/UI Test"
                }
                this.$kytos.$emit("showInfoPanel", content)
                // this.$kytos.$emit("hideInfoPanel")
            }
        },
        data() {
            return {
            }
        }
    }
    </script>

**k-status-bar**

============= ====== ================================== 
name          type   description                        
============= ====== ================================== 
statusMessage string Show a status message in StatusBar 
============= ====== ================================== 

