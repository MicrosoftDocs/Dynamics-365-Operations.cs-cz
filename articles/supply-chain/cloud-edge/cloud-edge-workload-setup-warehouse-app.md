---
title: Konfigurace mobilní aplikace Warehouse Management pro jednotky škálování cloudu a hraniční sítě
description: Tento článek vysvětluje, jak nastavit mobilní aplikace Warehouse Management pro sklady, které jsou obsluhovány cloudovou nebo hranovou jednotkou.
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
ms.openlocfilehash: 86edef2dfa6e9c71c04d50f185148be3a622fea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865231"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Konfigurace mobilní aplikace Warehouse Management pro jednotky škálování cloudu a hraniční sítě

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak nastavit mobilní aplikace Warehouse Management, aby je bylo možné použít ve skladech, které jsou obsluhovány cloudovou nebo hranovou jednotkou.

## <a name="prerequisites"></a>Předpoklady

Než začnete nastavovat svá mobilní zařízení pro připojení ke cloudové nebo hranové jednotce, ověřte, že se mohou připojit k podnikovému centru. Pokyny naleznete v části [Instalace a připojení mobilní aplikace Warehouse Management](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Další nastavení při spuštění mobilní aplikace Warehouse Management proti jednotce škálování

Jako součást [procesu nasazení pro úlohy jednotky škálování](cloud-edge-landing-page.md#scale-unit-manager-portal) většina dat, která jsou potřebná k připojení vašich zařízení s mobilní aplikací Warehouse Management, se automaticky synchronizuje z podnikového centra do jednotky škálování. Musíte však zadat data na stránce **Aplikace Azure Active Directory** stránka (**Správa systému \> Nastavení \> Aplikace Azure Active Directory**) v nasazení jednotky škálování. Navíc možná budete muset aktualizovat výchozí hodnotu **Společnost** pro ID uživatele nebo vytvořit nového uživatele. Uživatelé, kteří jsou přidruženi ke společnosti, která v nasazení jednotky škálování neexistuje, se nebudou moci přihlásit, když je k této jednotce škálování připojena mobilní aplikace Warehouse Management.

> [!NOTE]
> Protože data na stránce **Aplikace Azure Active Directory** nejsou synchronizována, musíte tato data ručně udržovat, pokud chcete přesunout úlohy skladu do jiné jednotky škálování.

Pamatujte, že v rámci nastavení připojení každé mobilní aplikace Warehouse Management musí být zadaná adresa URL Azure Active Directory pro jednotku škálování, nikoli pro podnikové centrum.
