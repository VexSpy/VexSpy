# VexSpy

**VexSpy** is a licensed remote administration and support workspace designed for controlled, permission-based device management. It combines a secure license portal, a lightweight updater, a desktop viewer application, and a generated endpoint client into one complete workflow for authorized users.

VexSpy is built around a simple idea: customers should be able to activate their license, download the latest application, generate their endpoint client, connect devices, and manage sessions from a clean interface without manually handling complicated setup steps.

> VexSpy is intended only for authorized environments, owned devices, customer-approved support scenarios, and legitimate administrative use.

---

## What VexSpy Provides

VexSpy is not just a single executable. It is a complete ecosystem made of several connected parts:

- **Web License Portal**
- **Updater / Launcher**
- **VexSpy Viewer**
- **Generated Endpoint Client**
- **License and HWID validation**
- **Ticket-based purchase and support flow**
- **Remote session tools**
- **Build and packaging system**

Each part has a specific role, and together they create a full customer-facing application flow.

---

## Web Portal

The VexSpy website acts as the public and administrative control layer of the system.

Customers can use the website to:

- Read product information
- Download the updater
- Purchase access
- Open support tickets
- Track purchase or support requests
- Log in with a license key
- View license-related information

Administrators can use the portal to:

- Create and manage licenses
- Review license status
- Track activations
- Reset HWID bindings when needed
- View audit logs
- Manage customer purchase tickets
- Respond to support requests
- Monitor suspicious or failed license activity

The portal supports multiple languages and is designed to provide a professional customer experience from purchase to activation.

---

## Purchase and Ticket System

VexSpy includes a manual purchase verification flow.

A customer first sends payment using one of the supported payment methods, then opens a ticket with the required details. The ticket system allows customers to select the type of request, such as:

- Payment
- Question
- Complaint
- Suggestion

For payment tickets, customers can include the payment method and transaction reference. For non-payment tickets, the form stays clean and only asks for the necessary message.

The ticket system is integrated with the admin panel, allowing administrators to review requests, reply to customers, update ticket status, and keep communication organized.

---

## Updater

The VexSpy Updater is the customer’s main entry point.

Instead of requiring users to manually download archives, extract files, or configure paths, the updater handles the release flow in a simple interface.

The updater can:

- Check license access
- Support free-mode access when enabled
- Download the latest `VexSpy.exe`
- Save the application directly to the user’s desktop
- Open VexSpy after download
- Repair the local copy by downloading it again
- Preserve the customer’s selected language and remembered license state

This makes the installation process easier for non-technical customers while keeping the license flow controlled.

---

## VexSpy Viewer

The VexSpy Viewer is the main desktop application.

It is the interface used to start the relay server, view connected devices, open sessions, generate endpoint clients, and use remote administration tools.

The viewer includes a branded startup experience, icon integration, multilingual UI, license checks, and a full session workspace. It is designed to feel like a complete desktop control panel rather than a collection of disconnected tools.

Core viewer areas include:

- Device list
- Relay server controls
- Session tabs
- User guide tab
- Generate EXE tool
- Remote desktop tools
- Camera tools
- Audio tools
- File transfer tools
- Terminal tools
- Process and service tools
- Diagnostics
- CMD logs
- Input audit

---

## Endpoint Client Generation

VexSpy can generate a standalone endpoint executable from inside the viewer.

During generation, the user provides the target relay IP and port. The generated client is then configured to connect back to the selected viewer relay. This allows each generated executable to be prepared for a specific deployment or support scenario.

The build system supports both visible console mode and hidden mode, depending on the intended authorized use case. Console mode is helpful for debugging, while hidden mode is cleaner for normal customer-side operation.

Generated clients are intended to be used only on systems where the operator has permission to run VexSpy.

---

## Remote Device Sessions

Once an endpoint client connects to the viewer relay, the device appears in the viewer’s device list. The operator can then open a session and access the available tools.

Sessions are tab-based, so multiple devices or multiple tools can be managed in an organized way.

The session interface is built to keep remote work readable and structured. Instead of forcing everything into one screen, VexSpy separates major workflows into dedicated tabs.

---

## Remote Desktop

The remote desktop module allows the viewer to receive screen frames from the connected endpoint and interact with the remote display.

It supports controlled remote viewing and session-based interaction for authorized support and administration workflows.

Typical uses include:

- Checking a remote desktop state
- Assisting a customer
- Performing administrative maintenance
- Reviewing application behavior
- Managing a connected endpoint visually

---

## Camera and Media Tools

VexSpy includes camera and media-related tools for environments where the connected device has appropriate hardware and permissions.

The camera module can list available cameras and start a camera stream when supported by the device.

The audio tools are designed to expose available audio devices and support controlled audio-related workflows where available.

Hardware-dependent features may vary depending on device drivers, permissions, Windows settings, and available devices.

---

## File Transfer

The file transfer module provides a two-sided file management experience.

It supports common file operations such as:

- Browsing local and remote files
- Uploading files
- Downloading files
- Creating folders
- Deleting files
- Managing transfer queues
- Pausing, resuming, or cancelling transfers
- Handling larger recursive transfers

This makes the viewer useful not only for visual sessions, but also for practical maintenance and support tasks.

---

## Terminal and CMD Logs

VexSpy includes terminal support for command-line administration.

Depending on the environment, the viewer can open different shell types such as CMD or PowerShell. Terminal output is shown in the viewer and can be tracked through the logging system.

The CMD Logs area records terminal-related events and runtime output from the endpoint client. This helps administrators understand what happened during a session, why a process exited, or what error occurred during operation.

Logs are especially useful for debugging generated clients, hidden-mode execution, restart behavior, and runtime errors.

---

## Diagnostics and System Tools

VexSpy includes several diagnostic and system inspection tools designed to help understand the state of a connected endpoint.

These may include:

- Device health information
- Process list
- Service list
- Clipboard-related actions
- System status checks
- Session diagnostics
- Connection state visibility

The goal is to give the operator enough context to solve support problems without switching between multiple tools.

---

## Licensing and HWID Protection

VexSpy uses a server-backed license system.

Licenses are validated through the web portal, and paid licenses can be bound to a hardware identity. This helps prevent the same license from being reused across multiple unauthorized machines.

The licensing system supports:

- License key verification
- Viewer name assignment
- HWID binding
- HWID mismatch detection
- Admin-side HWID reset
- Short-lived access tokens
- Runtime license validation
- Audit logs for license activity

If a license is used on a different device, the portal can record the event and reject access unless the administrator resets the HWID binding.

---

## Audit Logs

The portal includes audit logging for important activity.

Audit logs may include:

- License login attempts
- Failed license checks
- HWID mismatches
- Admin actions
- Ticket creation
- Ticket replies
- Download requests
- License updates
- Free-mode changes

This gives administrators better visibility into how the system is being used and helps identify configuration issues or suspicious behavior.

---

## Packaging and Distribution

VexSpy supports multiple packaging approaches for production distribution.

The project can be packaged through `.pyd` compilation and Nuitka-based executable builds. The goal is to distribute clean application executables while keeping source code out of customer-facing releases.

The updater downloads the final application executable directly, so customers do not need to manually extract archives or understand the internal package structure.

---

## Multilingual Experience

VexSpy is designed for international users.

The web portal, updater, and viewer include multilingual support so customers can interact with the system in their preferred language.

Supported interface languages include English, Turkish, Russian, Chinese, Spanish, Portuguese, German, French, Japanese, Korean, Arabic, and Polish.

---

## Typical Customer Flow

A normal customer flow looks like this:

1. The customer visits the VexSpy website.
2. The customer purchases access or opens a purchase ticket.
3. The administrator verifies the payment and prepares the license.
4. The customer downloads the VexSpy Updater.
5. The customer enters the license or uses free mode if enabled.
6. The updater downloads the latest VexSpy executable.
7. The customer opens VexSpy from the updater.
8. The operator starts the relay server in the viewer.
9. The operator generates an endpoint client for the target environment.
10. The authorized endpoint connects back to the viewer.
11. The operator opens a session and uses the available tools.

---

## Security and Responsible Use

VexSpy is designed for controlled and authorized use.

It should only be used in environments where the operator has permission to manage the target device. The project is intended for legitimate support, administration, diagnostics, and licensed customer workflows.

Unauthorized monitoring, access, or deployment is not an intended use of VexSpy.

---

## Summary

VexSpy combines a license portal, updater, viewer, endpoint generator, session workspace, remote tools, logging, and audit visibility into one complete system.

It is built to make remote administration easier to distribute, easier to activate, easier to support, and easier to manage from both the customer side and the administrator side.
