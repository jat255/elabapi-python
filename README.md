# elabapi-python

[![release](https://img.shields.io/pypi/v/elabapi-python.svg)](https://pypi.org/project/elabapi-python/)
[![wheel](https://img.shields.io/pypi/wheel/elabapi-python.svg)](https://pypi.org/project/elabapi-python/)

Python library for eLabFTW REST API.

# Description

This repository allows generating a python library to interact with [eLabFTW](https://github.com/elabftw/elabftw) REST API v2. It uses [Swagger Codegen](https://github.com/swagger-api/swagger-codegen/tree/3.0.0) to generate it based on the OpenApi specification of [eLabFTW REST API v2](https://doc.elabftw.net/api/v2/).

As such, it doesn't contain the generated code, but only instructions on how to generate it for local development.

Users should install the library with `pip`, as described below.

# Installation

~~~bash
pip install --user elabapi-python
~~~

# Usage

See the [examples folder](./examples).

# Dev

## Using the helper script

~~~bash
# generate the library
./helper.sh generate
# generate from local file: openapi.yaml must be in current dir
./helper.sh generate-from-local
# build packages
./helper.sh build
~~~

## Installing the library for dev

~~~bash
./helper.sh install-dev
~~~

## Publishing a new version

1. Bump version in config.json
2. Commit and push
3. Tag and push --tags
4. Create release on GitHub

# License

MIT, see [license file](./LICENSE).


## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/elabftw/elabapi-python.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/elabftw/elabapi-python.git`)

Then import the package:
```python
import elabapi_python 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import elabapi_python
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import time
import elabapi_python
from elabapi_python.rest import ApiException
from pprint import pprint

# Configure API key authorization: token
configuration = elabapi_python.Configuration()
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# create an instance of the API class
api_instance = elabapi_python.ApiKeysApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the API key

try:
    # Delete an API key.
    api_instance.delete_apikey(id)
except ApiException as e:
    print("Exception when calling ApiKeysApi->delete_apikey: %s\n" % e)

# Configure API key authorization: token
configuration = elabapi_python.Configuration()
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# create an instance of the API class
api_instance = elabapi_python.ApiKeysApi(elabapi_python.ApiClient(configuration))

try:
    # Read API keys
    api_response = api_instance.get_apikeys()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ApiKeysApi->get_apikeys: %s\n" % e)

# Configure API key authorization: token
configuration = elabapi_python.Configuration()
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# create an instance of the API class
api_instance = elabapi_python.ApiKeysApi(elabapi_python.ApiClient(configuration))
body = elabapi_python.ApikeysBody() # ApikeysBody |  (optional)

try:
    # Create an API key
    api_instance.post_apikeys(body=body)
except ApiException as e:
    print("Exception when calling ApiKeysApi->post_apikeys: %s\n" % e)
```

## Documentation for API Endpoints

All URIs are relative to *https://elab.local:3148/api/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ApiKeysApi* | [**delete_apikey**](docs/ApiKeysApi.md#delete_apikey) | **DELETE** /apikeys/{id} | Delete an API key.
*ApiKeysApi* | [**get_apikeys**](docs/ApiKeysApi.md#get_apikeys) | **GET** /apikeys | Read API keys
*ApiKeysApi* | [**post_apikeys**](docs/ApiKeysApi.md#post_apikeys) | **POST** /apikeys | Create an API key
*CommentsApi* | [**delete_entity_comment**](docs/CommentsApi.md#delete_entity_comment) | **DELETE** /{entity_type}/{id}/comments/{subid} | Delete an entity comment.
*CommentsApi* | [**patch_entity_comment**](docs/CommentsApi.md#patch_entity_comment) | **PATCH** /{entity_type}/{id}/comments/{subid} | Modify an entity comment.
*CommentsApi* | [**post_entity_comments**](docs/CommentsApi.md#post_entity_comments) | **POST** /{entity_type}/{id}/comments | Create a comment.
*CommentsApi* | [**read_entity_comment**](docs/CommentsApi.md#read_entity_comment) | **GET** /{entity_type}/{id}/comments/{subid} | Read a comment of that entity.
*CommentsApi* | [**read_entity_comments**](docs/CommentsApi.md#read_entity_comments) | **GET** /{entity_type}/{id}/comments | Read all comments of that entity.
*ConfigApi* | [**delete_config**](docs/ConfigApi.md#delete_config) | **DELETE** /config | Reset the config to default values
*ConfigApi* | [**get_config**](docs/ConfigApi.md#get_config) | **GET** /config | Read the config
*ConfigApi* | [**patch_config**](docs/ConfigApi.md#patch_config) | **PATCH** /config | Modify the config
*EventsApi* | [**delete_event**](docs/EventsApi.md#delete_event) | **DELETE** /event/{id} | Delete a booking slot.
*EventsApi* | [**patch_event**](docs/EventsApi.md#patch_event) | **PATCH** /events/{id} | Modify a booking slot. Warning: only one value (target) can be edited at a time. 
*EventsApi* | [**post_events**](docs/EventsApi.md#post_events) | **POST** /events/{id} | Create an event for the item specified as id.
*EventsApi* | [**read_events**](docs/EventsApi.md#read_events) | **GET** /events | Read all events in the team.
*ExperimentsApi* | [**delete_experiment**](docs/ExperimentsApi.md#delete_experiment) | **DELETE** /experiments/{id} | Delete an experiment.
*ExperimentsApi* | [**get_experiment**](docs/ExperimentsApi.md#get_experiment) | **GET** /experiments/{id} | Read an experiment
*ExperimentsApi* | [**patch_experiment**](docs/ExperimentsApi.md#patch_experiment) | **PATCH** /experiments/{id} | Modify an experiment
*ExperimentsApi* | [**post_experiment**](docs/ExperimentsApi.md#post_experiment) | **POST** /experiments | Create an experiment
*ExperimentsApi* | [**read_experiments**](docs/ExperimentsApi.md#read_experiments) | **GET** /experiments | Read all experiments that are accessible
*ExperimentsTemplatesApi* | [**delete_experiment_template**](docs/ExperimentsTemplatesApi.md#delete_experiment_template) | **DELETE** /experiments_templates/{id} | Delete an experiment template.
*ExperimentsTemplatesApi* | [**get_experiment_template**](docs/ExperimentsTemplatesApi.md#get_experiment_template) | **GET** /experiments_templates/{id} | Read an experiment template
*ExperimentsTemplatesApi* | [**patch_experiment_template**](docs/ExperimentsTemplatesApi.md#patch_experiment_template) | **PATCH** /experiments_templates/{id} | Modify an experiment template
*ExperimentsTemplatesApi* | [**post_experiment_template**](docs/ExperimentsTemplatesApi.md#post_experiment_template) | **POST** /experiments_templates | Create an experiment template
*ExperimentsTemplatesApi* | [**read_experiments_templates**](docs/ExperimentsTemplatesApi.md#read_experiments_templates) | **GET** /experiments_templates | Read all experiments_templates that are accessible
*FavoriteTagsApi* | [**delete_favtag**](docs/FavoriteTagsApi.md#delete_favtag) | **DELETE** /favtags/{id} | Unfavorite a tag.
*FavoriteTagsApi* | [**post_favtags**](docs/FavoriteTagsApi.md#post_favtags) | **POST** /favtags | Add a tag as favorite.
*FavoriteTagsApi* | [**read_favtags**](docs/FavoriteTagsApi.md#read_favtags) | **GET** /favtags | Read all favorite tags for the user.
*IdpsApi* | [**delete_idp**](docs/IdpsApi.md#delete_idp) | **DELETE** /idps/{id} | Delete an idp.
*IdpsApi* | [**patch_idp**](docs/IdpsApi.md#patch_idp) | **PATCH** /idps/{id} | Actions on an idp.
*IdpsApi* | [**post_idp**](docs/IdpsApi.md#post_idp) | **POST** /idps | Create an idp.
*IdpsApi* | [**read_idp**](docs/IdpsApi.md#read_idp) | **GET** /idps/{id} | Read an idp.
*IdpsApi* | [**read_idps**](docs/IdpsApi.md#read_idps) | **GET** /idps | Read all IDPs.
*ItemsApi* | [**delete_item**](docs/ItemsApi.md#delete_item) | **DELETE** /items/{id} | Delete an item.
*ItemsApi* | [**get_item**](docs/ItemsApi.md#get_item) | **GET** /items/{id} | Read an item
*ItemsApi* | [**patch_item**](docs/ItemsApi.md#patch_item) | **PATCH** /items/{id} | Modify an item
*ItemsApi* | [**post_item**](docs/ItemsApi.md#post_item) | **POST** /items | Create an item
*ItemsApi* | [**read_items**](docs/ItemsApi.md#read_items) | **GET** /items | Read all items that are accessible
*ItemsTypesApi* | [**delete_items_type**](docs/ItemsTypesApi.md#delete_items_type) | **DELETE** /items_types/{id} | Delete an item type.
*ItemsTypesApi* | [**get_items_type**](docs/ItemsTypesApi.md#get_items_type) | **GET** /items_types/{id} | Read an items type
*ItemsTypesApi* | [**patch_items_type**](docs/ItemsTypesApi.md#patch_items_type) | **PATCH** /items_types/{id} | Modify an item type
*ItemsTypesApi* | [**post_items_types**](docs/ItemsTypesApi.md#post_items_types) | **POST** /items_types | Create an item
*ItemsTypesApi* | [**read_items_types**](docs/ItemsTypesApi.md#read_items_types) | **GET** /items_types | Read all items_types that are accessible.
*LinksToExperimentsApi* | [**delete_entity_experiments_link**](docs/LinksToExperimentsApi.md#delete_entity_experiments_link) | **DELETE** /{entity_type}/{id}/experiments_links/{subid} | Delete an experiment link.
*LinksToExperimentsApi* | [**post_entity_experiments_links**](docs/LinksToExperimentsApi.md#post_entity_experiments_links) | **POST** /{entity_type}/{id}/experiments_links/{subid} | Create or import a link.
*LinksToExperimentsApi* | [**read_entity_experiments_links**](docs/LinksToExperimentsApi.md#read_entity_experiments_links) | **GET** /{entity_type}/{id}/experiments_links | Read all experiments links of that entity.
*LinksToItemsApi* | [**delete_entitiy_items_link**](docs/LinksToItemsApi.md#delete_entitiy_items_link) | **DELETE** /{entity_type}/{id}/items_links/{subid} | Delete an item link.
*LinksToItemsApi* | [**post_entity_items_links**](docs/LinksToItemsApi.md#post_entity_items_links) | **POST** /{entity_type}/{id}/items_links/{subid} | Create or import a link.
*LinksToItemsApi* | [**read_entity_items_links**](docs/LinksToItemsApi.md#read_entity_items_links) | **GET** /{entity_type}/{id}/items_links | Read all items links of that entity.
*NotificationsApi* | [**delete_notifications**](docs/NotificationsApi.md#delete_notifications) | **DELETE** /users/{id}/notifications | Delete all notifications of the user.
*NotificationsApi* | [**patch_notification**](docs/NotificationsApi.md#patch_notification) | **PATCH** /users/{id}/notifications/{subid} | Actions on a notification. Only changing &#x60;is_ack&#x60; column is possible. 
*NotificationsApi* | [**read_notification**](docs/NotificationsApi.md#read_notification) | **GET** /users/{id}/notifications/{subid} | Read a notification.
*NotificationsApi* | [**read_notifications**](docs/NotificationsApi.md#read_notifications) | **GET** /users/{id}/notifications | Read notifications of a user.
*StatusApi* | [**delete_status**](docs/StatusApi.md#delete_status) | **DELETE** /teams/{id}/status/{subid} | Delete a status.
*StatusApi* | [**patch_status**](docs/StatusApi.md#patch_status) | **PATCH** /teams/{id}/status/{subid} | Modify a status.
*StatusApi* | [**post_team_one_status**](docs/StatusApi.md#post_team_one_status) | **POST** /teams/{id}/status | Create a new status.
*StatusApi* | [**read_team_one_status**](docs/StatusApi.md#read_team_one_status) | **GET** /teams/{id}/status/{subid} | Read a status.
*StatusApi* | [**read_team_status**](docs/StatusApi.md#read_team_status) | **GET** /teams/{id}/status | Read status of a team.
*StepsApi* | [**delete_step**](docs/StepsApi.md#delete_step) | **DELETE** /{entity_type}/{id}/steps/{subid} | Delete a step.
*StepsApi* | [**patch_step**](docs/StepsApi.md#patch_step) | **PATCH** /{entity_type}/{id}/steps/{subid} | Actions on a step. 
*StepsApi* | [**post_step**](docs/StepsApi.md#post_step) | **POST** /{entity_type}/{id}/steps | Create a step.
*StepsApi* | [**read_steps**](docs/StepsApi.md#read_steps) | **GET** /{entity_type}/{id}/steps | Read all steps of that entity.
*TagsApi* | [**delete_tag**](docs/TagsApi.md#delete_tag) | **DELETE** /{entity_type}/{id}/tags/{subid} | Delete all tags.
*TagsApi* | [**patch_tag**](docs/TagsApi.md#patch_tag) | **PATCH** /{entity_type}/{id}/tags/{subid} | Actions on a tag (like removing it from the entity). 
*TagsApi* | [**post_tag**](docs/TagsApi.md#post_tag) | **POST** /{entity_type}/{id}/tags | Create a tag.
*TagsApi* | [**read_tag**](docs/TagsApi.md#read_tag) | **GET** /{entity_type}/{id}/tags/{subid} | Read a tag.
*TagsApi* | [**read_tags**](docs/TagsApi.md#read_tags) | **GET** /{entity_type}/{id}/tags | Read all tags of that entity.
*TeamTagsApi* | [**delete_team_tag**](docs/TeamTagsApi.md#delete_team_tag) | **DELETE** /team_tags/{id} | Delete a tag.
*TeamTagsApi* | [**patch_tags**](docs/TeamTagsApi.md#patch_tags) | **PATCH** /team_tags | Actions on tags. 
*TeamTagsApi* | [**patch_team_tag**](docs/TeamTagsApi.md#patch_team_tag) | **PATCH** /team_tags/{id} | Actions on a tag. 
*TeamTagsApi* | [**post_team_tag**](docs/TeamTagsApi.md#post_team_tag) | **POST** /team_tags | Create a tag in the team.
*TeamTagsApi* | [**read_team_tag**](docs/TeamTagsApi.md#read_team_tag) | **GET** /team_tags/{id} | Read a tag.
*TeamTagsApi* | [**read_team_tags**](docs/TeamTagsApi.md#read_team_tags) | **GET** /team_tags | Read all tags for the team.
*TeamgroupsApi* | [**delete_teamgroup**](docs/TeamgroupsApi.md#delete_teamgroup) | **DELETE** /teams/{id}/teamgroups/{subid} | Delete a teamgroup.
*TeamgroupsApi* | [**patch_teamgroup**](docs/TeamgroupsApi.md#patch_teamgroup) | **PATCH** /teams/{id}/teamgroups/{subid} | Modify a teamgroup.
*TeamgroupsApi* | [**post_teamgroups**](docs/TeamgroupsApi.md#post_teamgroups) | **POST** /teams/{id}/teamgroups | Create a new teamgroup.
*TeamgroupsApi* | [**read_team_teamgroups**](docs/TeamgroupsApi.md#read_team_teamgroups) | **GET** /teams/{id}/teamgroups | Read teamgroups of a team.
*TeamgroupsApi* | [**read_teamgroup**](docs/TeamgroupsApi.md#read_teamgroup) | **GET** /teams/{id}/teamgroups/{subid} | Read a teamgroup.
*TeamsApi* | [**patch_team**](docs/TeamsApi.md#patch_team) | **PATCH** /teams/{id} | Actions on a team. 
*TeamsApi* | [**post_teams**](docs/TeamsApi.md#post_teams) | **POST** /teams | Create a new team.
*TeamsApi* | [**read_team**](docs/TeamsApi.md#read_team) | **GET** /teams/{id} | Read a team. Requires Admin permissions.
*TeamsApi* | [**read_teams**](docs/TeamsApi.md#read_teams) | **GET** /teams | Read all teams. Requires Sysadmin permissions.
*TodolistApi* | [**delete_todoitem**](docs/TodolistApi.md#delete_todoitem) | **DELETE** /todolist/{id} | Delete a todoitem.
*TodolistApi* | [**patch_todoitem**](docs/TodolistApi.md#patch_todoitem) | **PATCH** /todolist/{id} | Actions on a todoitem. 
*TodolistApi* | [**post_todolist**](docs/TodolistApi.md#post_todolist) | **POST** /todolist | Create a todo item
*TodolistApi* | [**read_todoitem**](docs/TodolistApi.md#read_todoitem) | **GET** /todolist/{id} | Read a todo entry.
*TodolistApi* | [**read_todolist**](docs/TodolistApi.md#read_todolist) | **GET** /todolist | Read all todoitems.
*UnfinishedStepsApi* | [**read_unfinished_steps**](docs/UnfinishedStepsApi.md#read_unfinished_steps) | **GET** /unfinished_steps | Read all unfinished steps.
*UploadsApi* | [**delete_upload**](docs/UploadsApi.md#delete_upload) | **DELETE** /{entity_type}/{id}/uploads/{subid} | Delete an upload.
*UploadsApi* | [**patch_upload**](docs/UploadsApi.md#patch_upload) | **PATCH** /{entity_type}/{id}/uploads/{subid} | Actions on an upload. 
*UploadsApi* | [**post_upload**](docs/UploadsApi.md#post_upload) | **POST** /{entity_type}/{id}/uploads | Create an upload.
*UploadsApi* | [**post_upload_replace**](docs/UploadsApi.md#post_upload_replace) | **POST** /{entity_type}/{id}/uploads/{subid} | Replace an existing uploaded file. The existing file will be archived and the new one will be added.
*UploadsApi* | [**read_upload**](docs/UploadsApi.md#read_upload) | **GET** /{entity_type}/{id}/uploads/{subid} | Read an upload.
*UploadsApi* | [**read_uploads**](docs/UploadsApi.md#read_uploads) | **GET** /{entity_type}/{id}/uploads | Read attached files of that entity.
*UsersApi* | [**patch_user**](docs/UsersApi.md#patch_user) | **PATCH** /users/{id} | Modify a user.
*UsersApi* | [**post_user**](docs/UsersApi.md#post_user) | **POST** /users | Create a new user.
*UsersApi* | [**read_user**](docs/UsersApi.md#read_user) | **GET** /users/{id} | Read information of a user.
*UsersApi* | [**read_users**](docs/UsersApi.md#read_users) | **GET** /users | Read users from instance.

## Documentation For Models

 - [Apikey](docs/Apikey.md)
 - [ApikeysBody](docs/ApikeysBody.md)
 - [Comment](docs/Comment.md)
 - [Config](docs/Config.md)
 - [Entity](docs/Entity.md)
 - [Event](docs/Event.md)
 - [EventsIdBody](docs/EventsIdBody.md)
 - [EventsIdBody1](docs/EventsIdBody1.md)
 - [EventsidDelta](docs/EventsidDelta.md)
 - [Experiment](docs/Experiment.md)
 - [ExperimentTemplate](docs/ExperimentTemplate.md)
 - [ExperimentsBody](docs/ExperimentsBody.md)
 - [ExperimentsIdBody](docs/ExperimentsIdBody.md)
 - [ExperimentsLinksSubidBody](docs/ExperimentsLinksSubidBody.md)
 - [ExperimentsTemplatesBody](docs/ExperimentsTemplatesBody.md)
 - [ExperimentsTemplatesIdBody](docs/ExperimentsTemplatesIdBody.md)
 - [FavtagsBody](docs/FavtagsBody.md)
 - [Id](docs/Id.md)
 - [Id1](docs/Id1.md)
 - [Id2](docs/Id2.md)
 - [Id3](docs/Id3.md)
 - [IdCommentsBody](docs/IdCommentsBody.md)
 - [IdStatusBody](docs/IdStatusBody.md)
 - [IdStepsBody](docs/IdStepsBody.md)
 - [IdTagsBody](docs/IdTagsBody.md)
 - [IdTeamgroupsBody](docs/IdTeamgroupsBody.md)
 - [IdUploadsBody](docs/IdUploadsBody.md)
 - [Idp](docs/Idp.md)
 - [IdpsBody](docs/IdpsBody.md)
 - [IdpsIdBody](docs/IdpsIdBody.md)
 - [InlineResponse200](docs/InlineResponse200.md)
 - [InlineResponse2001](docs/InlineResponse2001.md)
 - [InlineResponse2002](docs/InlineResponse2002.md)
 - [InlineResponse2003](docs/InlineResponse2003.md)
 - [Item](docs/Item.md)
 - [ItemsBody](docs/ItemsBody.md)
 - [ItemsIdBody](docs/ItemsIdBody.md)
 - [ItemsLinksSubidBody](docs/ItemsLinksSubidBody.md)
 - [ItemsType](docs/ItemsType.md)
 - [ItemsTypesBody](docs/ItemsTypesBody.md)
 - [Link](docs/Link.md)
 - [Notification](docs/Notification.md)
 - [Status](docs/Status.md)
 - [Step](docs/Step.md)
 - [StepsSubidBody](docs/StepsSubidBody.md)
 - [Tag](docs/Tag.md)
 - [TagsSubidBody](docs/TagsSubidBody.md)
 - [Team](docs/Team.md)
 - [TeamTagsBody](docs/TeamTagsBody.md)
 - [TeamTagsBody1](docs/TeamTagsBody1.md)
 - [TeamTagsIdBody](docs/TeamTagsIdBody.md)
 - [Teamgroup](docs/Teamgroup.md)
 - [TeamgroupUsers](docs/TeamgroupUsers.md)
 - [TeamgroupsSubidBody](docs/TeamgroupsSubidBody.md)
 - [TeamsBody](docs/TeamsBody.md)
 - [Todoitem](docs/Todoitem.md)
 - [TodolistBody](docs/TodolistBody.md)
 - [TodolistIdBody](docs/TodolistIdBody.md)
 - [UnfinishedStep](docs/UnfinishedStep.md)
 - [UnfinishedSteps](docs/UnfinishedSteps.md)
 - [Upload](docs/Upload.md)
 - [UploadsSubidBody](docs/UploadsSubidBody.md)
 - [Users](docs/Users.md)
 - [UsersBody](docs/UsersBody.md)
 - [UsersIdBody](docs/UsersIdBody.md)

## Documentation For Authorization


## token

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Author


