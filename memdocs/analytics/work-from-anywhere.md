---
title: Work from anywhere (preview) report in Endpoint analytics
titleSuffix: Microsoft Endpoint Manager
description: The Work from anywhere (preview) report in Endpoint analytics provides insights to help your end users be productive from anywhere.
ms.date: 10/19/2021
ms.prod: configuration-manager
ms.technology: configmgr-analytics
ms.topic: conceptual
author: mestew
ms.author: mstewart
manager: dougeby
ms.localizationpriority: high
---

# Work from anywhere (preview) report
<!--8668496-->
The ability for employees to work from anywhere productively is essential in today’s world. This report offers insights into how prepared your workforce is to be productive from anywhere. The **Work from anywhere** report is an evolution of the [Recommended software report](recommended-software.md). You may notice changes in your scores because the calculations are different in the **Work from anywhere** report.  From this report, you can review your scores and how they compare to the selected baseline. Learn how to improve your scores by reviewing the insights and recommendations for each of them.  

## <a name="bkmk_score"></a> Work from anywhere score

The **Work from anywhere score** is a number between 0 and 100. The score represents a weighted average of the percent of devices that have deployed the various insights for helping your end users be productive from anywhere. The score is computed for all Intune and Configuration Manager devices that have opted into [Endpoint analytics](overview.md).

The following metrics are weighted and used to compute the **Work from anywhere score**:

- [Windows](#windows)
- [Cloud management](#bkmk_management)
- [Cloud identity](#bkmk_identity)
- [Cloud provisioning](#bkmk_provisioning)

:::image type="content" source="media/8668496-work-from-anywhere-score.png" alt-text="Screenshot of the Work from anywhere report showing the scores and metrics" lightbox="media/8668496-work-from-anywhere-score.png":::
## Windows

Newer versions of Windows provide a better user experience than older versions of Windows. The **Windows** metric measures the percent of devices on supported versions of Windows. The recommended remediation actions vary depending on how the devices are managed. For Intune and co-managed devices, use Intune to [move devices to an updated version of Windows](../intune/protect/windows-10-feature-updates.md). For Configuration Manager devices, create a deployment plan using [Desktop Analytics](../configmgr/desktop-analytics/overview.md). Your score is based on if these remediation actions have been completed or not.

For information about the cost savings and benefits enabled by Windows, download the [TEI whitepaper](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWCpaP).

:::image type="content" source="media/8668496-windows.png" alt-text="Screenshot of the Windows fly out showing graph and insights" lightbox="media/8668496-windows.png":::

## <a name="bkmk_management"></a> Cloud management

Configuration Manager and Intune provide integrated cloud-powered management tools and unique co-management options to provision, deploy, manage, and secure endpoints and applications across an organization. With the power of cloud management, you can achieve several productivity benefits. Your end-users benefit when they can access corporate resources away from the corporate network. Eliminating the need for and performance overhead of Group Policy also results in a better end-user experience.

The **Cloud management** metric measures the percent of PCs that have attached to the Microsoft 365 cloud to unlock additional capabilities. There are multiple recommended actions for co-managed devices and their workloads, CMG, and tenant attached devices. See how [Microsoft is enabling modern management for our employees](https://www.microsoft.com/en-us/itshowcase/managing-windows-10-devices-with-microsoft-intune).

Benefits of each cloud management type:<!--IN7207657-->

|Benefits|[**Cloud management gateway (CMG)**](../configmgr/core/clients/manage/cmg/overview.md)|[**Tenant attach**](../configmgr/tenant-attach/device-sync-actions.md)|[**Co-management**](../configmgr/comanage/overview.md)|[**Intune**](../intune/fundamentals/what-is-intune.md)|
|---|---|---|---|---|
| Manage your clients anywhere | :::image type="content" source="media/green-check.png" border="false" alt-text="Yes."::: | :::image type="content" source="media/green-check.png" border="false" alt-text="Yes."::: | :::image type="content" source="media/green-check.png" border="false" alt-text="Yes."::: | :::image type="content" source="media/green-check.png" border="false" alt-text="Yes."::: |
| View and take action on all Windows PCs from Microsoft Endpoint Manager admin center| |:::image type="content" source="media/green-check.png" border="false" alt-text="Yes.":::| :::image type="content" source="media/green-check.png" border="false" alt-text="Yes.":::| :::image type="content" source="media/green-check.png" border="false" alt-text="Yes."::: |
| Modernize your directory approach with Azure AD | |:::image type="content" source="media/green-check.png" border="false" alt-text="Yes.":::| :::image type="content" source="media/green-check.png" border="false" alt-text="Yes.":::| :::image type="content" source="media/green-check.png" border="false" alt-text="Yes."::: |
|Enhance Zero Trust with conditional access| | |:::image type="content" source="media/green-check.png" border="false" alt-text="Yes.":::| :::image type="content" source="media/green-check.png" border="false" alt-text="Yes."::: |
| Make device provisioning easier by enabling Windows Autopilot |  | |:::image type="content" source="media/green-check.png" border="false" alt-text="Yes.":::| :::image type="content" source="media/green-check.png" border="false" alt-text="Yes."::: |
| Gain additional remote access with Intune | | |:::image type="content" source="media/green-check.png" border="false" alt-text="Yes.":::| :::image type="content" source="media/green-check.png" border="false" alt-text="Yes."::: |
| Split PC management workloads between cloud and on-premises | | |:::image type="content" source="media/green-check.png" border="false" alt-text="Yes.":::| |
| Simplify PC and driver updating with the cloud | | |:::image type="content" source="media/green-check.png" border="false" alt-text="Yes.":::| :::image type="content" source="media/green-check.png" border="false" alt-text="Yes."::: |
| Consistent end-user experience for managing enrolled devices and installed apps | | |:::image type="content" source="media/green-check.png" border="false" alt-text="Yes.":::| :::image type="content" source="media/green-check.png" border="false" alt-text="Yes."::: |
| Reduce complexity with always up-to-date cloud only infrastructure | :::image type="content" source="media/green-check.png" border="false" alt-text="Yes."::: | | | :::image type="content" source="media/green-check.png" border="false" alt-text="Yes."::: |

## <a name="bkmk_identity"></a> Cloud identity

Cloud identity provides users with many productivity benefits including device-wide single sign-on to apps and services, Windows Hello sign-in, self-service BitLocker recovery, and corporate data roaming. The **Cloud identity** metric measures the percent of devices enrolled in Azure Active Directory (AD) or hybrid Azure AD. Your Intune and co-managed devices are already enrolled in Azure AD. The recommended remediation action for devices managed by Configuration Manager is to [enroll them in hybrid Azure AD](/azure/active-directory/devices/hybrid-azuread-join-managed-domains).


:::image type="content" source="media/8668496-cloud-identity.png" alt-text="Screenshot of the Cloud identity fly out showing insights for the metric" lightbox="media/8668496-cloud-identity.png":::

## <a name="bkmk_provisioning"></a> Cloud provisioning

Cloud provisioning provides a simpler initial provisioning experience for Windows PCs than the native experience. It reduces the number of screens in the Out Of Box Experience (OOBE) and provides defaults, to ensure the device is correctly provisioning from the factory or on reset. The **Cloud provisioning** metric measures the percentage of machines that are either Windows 365 Cloud PCs or Windows Intune devices that are both registered and have a deployment profile created for Autopilot. The recommended remediation actions are to register and create deployment profiles for existing devices in Windows Autopilot using Microsoft [Intune](../autopilot/enrollment-autopilot.md).


:::image type="content" source="media/8668496-cloud-provisioning.png" alt-text="Screenshot of the cloud provisioning tab showing the device list" lightbox="media/8668496-cloud-provisioning.png":::

## <a name="bkmk_windows11"></a> Windows 11 hardware readiness
<!--IN9740163-->
The **Windows** metric provides Windows 11 hardware readiness insights for devices that are enrolled via Intune, co-management, or Configuration Manager version 2107 or newer with tenant attach enabled. To determine how many of your enrolled devices meet the [minimum system requirements](/windows/whats-new/windows-11-requirements#hardware-requirements) for Windows 11, select **Windows** to open the flyout on the **Overview** page in **Work from anywhere**. A chart is displayed showing which specific hardware requirements are the top blockers in your organization.

:::image type="content" source="media/windows-hardware.png" alt-text="Screenshot of the Windows flyout that displays a chart showing top hardware blockers in your organization." lightbox="media/windows-hardware.png":::

In the **Windows** tab, a device-by-device view of Windows 11 hardware readiness is displayed. The **Windows 11 readiness status** column indicates whether a device is **Capable** or **Not capable** of upgrading to Windows 11 based on the minimum system requirements. The column also lists if a device is already **Upgraded** or if the status is **Unknown** for a device. The **Windows 11 readiness reason** column outlines the specific hardware requirements that aren't met for devices that have a readiness status of **Not capable**.

> [!NOTE]
> - In most cases, devices with a Windows 11 readiness status of **Unknown** are simply inactive. To verify this, review the [last check in time](/troubleshoot/mem/intune/troubleshoot-policies-in-microsoft-intune) from Intune. If you see a large number of inactive devices in the report, consider adjusting your [device clean up rules](../intune/remote-actions/devices-wipe.md#automatically-delete-devices-with-cleanup-rules), or target only active devices with the [Intune data collection policy](enroll-intune.md#bkmk_onboard) that controls Endpoint analytics enrollment. 
> - Windows 11 hardware readiness insights do not impact your Work from anywhere score.

## <a name="bkmk_np"></a> No commercial median

The built-in baseline of **All organizations (median)** doesn't currently have metrics for the subscore metrics listed in the sections above.

## Next steps

- View [Startup performance](startup-performance.md)
- Use [Proactive remediations](proactive-remediations.md) to help fix common support issues before end-users notice issues.
