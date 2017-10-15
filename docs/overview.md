Metaroom is a collection of libraries and utilities that enable NAF rooms composed of apps from different clients.

# Projects

## Functionality

### naf-persist
Persists entities and their components into a database. It can optionally track an entity's private components.

### naf-multi-schema
A NAF schema that syncs many basic components of an entity such as geometry and material. This is meant to be applied to non-naf apps so they can be easily networked.

### component-by-selector
Allows components (or mixins) to be applied to elements through a css selector. The intention here is to auto apply the naf-multi-schema component to non NAF apps.

### naf-auth
Provides auth support for NAF clients. This would probably be a This plugin could be quired for a client's authenticated ID.

## Plugins
### naf-chat
A simple chat utility. Will have a component that displays chat messages in the scene, and a NAF plugin for sending chat message events.

## Events
Plugins that allow clients to trigger events on apps in other clients, such as clicking, would allow interactive non-naf apps to better function in a NAF room.  The design of plugins/projects that enable this needs to be thought out more, check out events.md for current thoughts on the matter.

## Component Syncing Related
It would be nice to have more granular control on the syncing of components. This includes whether a component gets sent, whether it is accepted when received, and constraints on properties of the component.

This hasn't been fleshed out enough to define projects yet, but check out componentsyncthoughts.md for more thoughts on the matter.

## Tools
### NAF Inspector
An interface that shows connected NAF clients and their entities. Will be pluggable to allow NAF plugins to show parameters they may be storing about clients. naf-auth for instance, could show the user's authenticated id.

# Usage Patterns

### naf-multi-schema components-by-selector
This setup allows non-naf scenes to easily be converted to naf ones. This setup is one of the quickest ways to build an interesting metaroom. Without networked events or persisting, this is limited though.