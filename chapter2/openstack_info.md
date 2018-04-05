### Introduction to OpenStack

Hundreds of times you may have listened that ManageIQ is manager of managers. And these managers then eventually will be known as **components** or **providers**. Since this project is concerned with infrastruture management , that's why OpenStack comes into the picture with Infrastructure-As-Provider role within ManageIQ.

### How ManageIQ controls the integrated environment?

ManageIQ collects inventory information like request VMs, networking images from the OpenStack provider. ManageIQ uses REST API to communicate with OpenStack and further OpenStack uses REST API to communicate with its communicate.
