---
title: Konfigurace mobilní aplikace Warehouse Management pro jednotky škálování cloudu a hraniční sítě
description: Toto téma vysvětluje, jak nastavit mobilní aplikace Warehouse Management pro sklady, které jsou obsluhovány cloudovou nebo hranovou jednotkou.
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 1fa00b40db2f6246029876964dca9d3229567848
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071625"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Konfigurace mobilní aplikace Warehouse Management pro jednotky škálování cloudu a hraniční sítě

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit mobilní aplikace Warehouse Management, aby je bylo možné použít ve skladech, které jsou obsluhovány cloudovou nebo hranovou jednotkou.

## <a name="prerequisites"></a>Předpoklady

Než začnete nastavovat svá mobilní zařízení pro připojení ke cloudové nebo hranové jednotce, ověřte, že se mohou připojit k podnikovému centru. Pokyny naleznete v části [Instalace a připojení mobilní aplikace Warehouse Management](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Další nastavení při spuštění mobilní aplikace Warehouse Management proti jednotce škálování

Jako součást [procesu nasazení pro úlohy jednotky škálování](cloud-edge-landing-page.md#scale-unit-manager-portal) většina dat, která jsou potřebná k připojení vašich zařízení s mobilní aplikací Warehouse Management, se automaticky synchronizuje z podnikového centra do jednotky škálování. Musíte však zadat data na stránce **Aplikace Azure Active Directory** stránka (**Správa systému \> Nastavení \> Aplikace Azure Active Directory**) v nasazení jednotky škálování. Navíc možná budete muset aktualizovat výchozí hodnotu **Společnost** pro ID uživatele nebo vytvořit nového uživatele. Uživatelé, kteří jsou přidruženi ke společnosti, která v nasazení jednotky škálování neexistuje, se nebudou moci přihlásit, když je k této jednotce škálování připojena mobilní aplikace Warehouse Management.

> [!NOTE]
> Protože data na stránce **Aplikace Azure Active Directory** nejsou synchronizována, musíte tato data ručně udržovat, pokud chcete přesunout úlohy skladu do jiné jednotky škálování.

Pamatujte, že v rámci nastavení připojení každé mobilní aplikace Warehouse Management musí být zadaná adresa URL Azure Active Directory pro jednotku škálování, nikoli pro podnikové centrum.
