# Examples
@anchor Examples

Mesh devices are broadly categorized into two roles: a provisioner role and a node role. 
The nRF5 SDK for Mesh provides several example projects to demonstrate these roles, mesh models, and certain features that will
help you get started on new mesh-based projects.

## Read before testing
Before you start using the examples, see the following pages:
- [Installing the toolchain](@ref md_doc_getting_started_how_to_toolchain)
- [Building the mesh stack and examples](@ref md_doc_getting_started_how_to_build)
- [Running examples](@ref md_doc_getting_started_how_to_run_examples)

You can also quickly run an example without going through the complete toolchain installation.
See [Running a first example](@ref md_doc_getting_started_mesh_quick_start) for details.

In the nRF5 SDK for Mesh v3.2.0, [experimental support for the S113 SoftDevice](@ref compatibility_s113)
has been added to various examples, except for the @ref md_examples_experimental_lpn_README
and @ref md_examples_sdk_coexist_README.

## Available examples
The following examples are provided with this SDK:

* @subpage md_examples_light_switch_README is a mesh ecosystem example
  that contains four smaller examples: provisioner, client, server, and proxy-server.

* @subpage md_examples_enocean_switch_README demonstrates how to implement a third party device in Mesh ecosystem,
  namely an EnOcean-to-Mesh translator. The EnOcean switches send the button status using BLE advertising packets.
  These packets can be captured and can be used to generate equivalent mesh messages for controlling other mesh nodes.

* @subpage md_examples_beaconing_README implements custom beacon advertising
  and shows how to send and receive custom packets using the nRF5 SDK for Mesh.

* @subpage md_examples_dfu_README shows how to use the mesh DFU framework to update the firmware of a device over the mesh.

* @subpage md_examples_serial_README demonstrates how to  use the serial interface to create a mesh connectivity device.

* @subpage md_examples_sdk_coexist_README demonstrate how the nRF5 SDK features can be simultaneously used with nRF5 SDK for Mesh.

Moreover, the SDK comes with several @subpage md_examples_experimental_examples, such as:

* @ref md_examples_experimental_dimming_README demonstrate how to use [Generic Level model](@ref GENERIC_LEVEL_MODEL)
  APIs in an application to implement dimming light and corresponding dimmer switch.
* @ref md_examples_experimental_lpn_README demonstrates the Low Power node feature.
* @ref md_examples_pb_remote_README demonstrates the use of remote provisioning to provision devices outside of the provisioner's radio range.

## Common example modules @anchor common-modules

The examples implement common functionalities through several common modules, including among others:
- simple hardware abstraction layer,
- RTT input functionality that uses the nRF5 SDK @link_app_timer and enables the examples to poll [RTT](@ref segger-rtt) for input characters,
- Mesh stack and SoftDevice initialization helper modules,
- behaviors for several generic models.

For full overview of all common modules and detailed information, check the \ref MESH_API_GROUP_APP_SUPPORT API section.
