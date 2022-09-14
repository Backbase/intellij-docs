# Backbase Service Toolkit

This IntelliJ Platform Plugin is going to help you to create and maintain your own Backbase backend services. It would make it easier for you to follow [Community Backbase Documentation](https://community.backbase.com/) with simple Intellij options. 

Following are ways you can use the plugin.

## Create a New Backbase Project

Create a new backbase service based on [core-service-archetype](https://community.backbase.com/documentation/ServiceSDK/latest/create_a_core_service).

<img src="img/new-project/1-new-project.png"  />

Fill out your project details.

<img src="img/new-project/2-project-details.png"  />

Select project location.

<img src="img/new-project/3-project-location.png"  />

This will create a maven project with `service-sdk-starter-core` as parent.

## Add SSDK Module

Right click on the project -> `Backbase` menu -> Add SSDK Module

<img src="img/ssdk-modules/1-menu.png" />

Select dependencies you want to include

<img src="img/ssdk-modules/2-options.png" />


## Add Persistence Support

Right click on the project -> `Backbase` menu -> Add Persistence Support

<img src="img/persistence/1-menu.png"  />

Select according to your needs

<img src="img/persistence/2-more-options.png"  />

Based on your choice in the previous step, require dependcies will be added to your pom.xml, liquidbase sample xml created etc.

<img src="img/persistence/3-result.png" />


## Events Support

### Define Event

Right click on the project -> `Backbase` menu -> Define Event

<img src="img/events/1-menu.png" />

Enter a name for your event

<img src="img/events/2-define-event.png" />

This will create a event json file and will add require dependencies to your pom.xml. Change the json with your needs and run `mvn install` to generate code.

<img src="img/events/3-json-mvn-install.png" />

You can generate code based on above event in your service class

<img src="img/events/4-emit-event-menu.png" />

Change the name according to the class generated in the previous step

<img src="img/events/5-generated-code.png" />

### Consume Events

Make sure you have already created an event json file as described in define events. 
If you are consuming events from other services, make sure you have copied the json contents from their repo to your own file.
Generate POJO's either by running `mvn install` or clikcing `Generate Sources` from maven tab in IntelliJ

Right click on the project -> `Backbase` menu -> Consume and Event

<img src="img/events/consume/1-consume-events.png"  />

This should open a box showing all the defined events. (Again whose code is generated, if not generate the code)

<img src="img/events/consume/2-consume-events-box.png" />

On selecting the class, it should generate a sample code for that

<img src="img/events/consume/3-generated-code.png" />

## Create a New Behaviour Extension Project

Behavior extensions enable you to customize the workflow of your service. Create a new [extensions project](https://community.backbase.com/documentation/ServiceSDK/latest/extend_service_behavior)

<img src="img/new-extension-project/1-new-project.png" />

Enter the details of the backbase service you want to extend that supports camel routes.

<img src="img/new-extension-project/2-bb-service-to-extend.png" />

Enter the maven details for the generated project

<img src="img/new-extension-project/3-project-details.png" />

Enter project location

<img src="img/new-extension-project/4-project-location.png" />

This will create a maven project with required dependencies and structure.

<img src="img/new-extension-project/5-result.png" />

Create a hook -> `Backbase` menu -> Generate new behaviour extension hooks 

<img src="img/new-extension-project/6-hooks-menu.png" />

Enter hook name and select route type

<img src="img/new-extension-project/7-hooks-details.png" />

Based on your above selection it will create require config class

<img src="img/new-extension-project/8-hooks-generated-class.png" />

## Open API Support

### Generate Client

To generate a client using the backbase-openapi tool. Specs for which clients need to be generated is already downloaded in the resources folder. Right click of a spec yaml 

<img src="img/openapi/1-generate-client-menu.png" />

Based on file selection, the dialog box will be populated accordingly. Change if needed

<img src="img/openapi/2-generate-client-package-details.png" />

It will add the necessary dependencies in pom and the boat maven plugin with execution. It will also create a configuration class. Run `mvn install` to generate code.

<img src="img/openapi/3-generate-client-config-file.png" />

### Generate API

Right click on the project -> `Backbase` menu -> Generate Server API From Openapi Specs

<img src="img/openapi/1-generate-server-api-menu.png" />

This should open file selection box , where you can select the spec to implment.
<img src="img/openapi/2-generate-server-api-select-spec.png" />

On selection, a Dialog box would open with opinionated values and file path.

<img src="img/openapi/3-generate-server-api-package-details.png" />
On selection, the required dependencies and plugin will be added in the pom.xml. Generated sources using `mvn install`

## Search Golden Samples

We have [Backbase Golden Sample](https://github.com/Backbase/golden-sample-services) example which includes best practices to work with microservices and Backbase SDKs. 

You can seach for a particular text from your project files

<img src="img/search/1-search.png" />

This will search the same in golden samples examples project

<img src="img/search/2-search-result.png" />