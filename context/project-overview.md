# wi-sub

## Overview

wi-sub is a mobile-first web application that allows a WiFi provider to manage users, assign devices via MAC addresses, configure WiFi networks, and track subscription durations with automated pricing and expiration notifications. The system replaces manual tracking (Excel, paper) with a structured, automated solution.

## Goals

1. Allow fast creation and management of users and their devices  
2. Automate subscription pricing, duration tracking, and expiration  
3. Provide real-time visibility on active and expired subscriptions  
4. Reduce manual errors and missed renewals  

## Core User Flow

1. Admin logs into the system (hardcoded credentials)  
2. Admin creates a user (name, phone, optional email)  
3. Admin registers one or more devices (MAC addresses)  
4. Admin assigns a device to a WiFi network  
5. Admin sets a subscription duration  
6. System calculates price automatically  
7. System tracks expiration date  
8. System sends notifications (admin + user if email exists)  

## Features

### User & Device Management

- Create, update, delete users  
- Assign multiple devices (MAC addresses) per user  
- Link devices to WiFi networks  

### WiFi Management

- Create, update, delete WiFi networks  
- Assign users/devices to specific WiFi  

### Subscription Management

- Set subscription duration (day/week/month/custom)  
- Automatic pricing calculation:
  - 1 day = 1,000 Ar  
  - 1 week = 5,000 Ar  
  - 1 month = 20,000 Ar  
- Track start and end dates  

### Notifications

- Admin notified:
  - 3 days before expiration  
  - On expiration  
- User notified (if email provided):
  - 3 days before expiration  
  - On expiration  

## Scope

### In Scope

- Admin dashboard (mobile-first)  
- CRUD for users, devices, WiFi  
- Subscription logic + pricing  
- Expiration tracking  
- Notifications (email + in-app)  

### Out of Scope

- Public user portal  
- Online payments integration  
- Multi-admin roles (single admin only)  

## Success Criteria

1. Admin can create a user and assign a subscription in < 1 minute  
2. System correctly calculates pricing for all durations  
3. Notifications trigger correctly before and on expiration  
4. All subscriptions are visible with status (active/expired)  