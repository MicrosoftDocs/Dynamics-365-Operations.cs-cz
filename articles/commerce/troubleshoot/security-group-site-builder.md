---
title: Během počátečního nasazení nelze konfigurovat skupinu zabezpečení pro Tvůrce webů Commerce
description: Toto téma obsahuje pokyny pro řešení potíží, které mohou pomoci, když skupina zabezpečení Microsoft Azure Active Directory (Azure AD) pro Tvůrce webů Commerce se při vytváření komponent elektronického obchodování nezobrazuje jako volba Microsoft Dynamics Lifecycle Services (LCS) během počátečního nasazení nového tenanta elektronického obchodování.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d29e560d0f7b2bbc2415d7a0f6fe18f2ca17dc7c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020725"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Během počátečního nasazení nelze konfigurovat skupinu zabezpečení pro Tvůrce webů Commerce

[!include [banner](../../includes/banner.md)]

Toto téma obsahuje pokyny pro řešení potíží, které mohou pomoci, když skupina zabezpečení Microsoft Azure Active Directory (Azure AD) pro Tvůrce webů Commerce se při vytváření komponent elektronického obchodování nezobrazuje jako volba Microsoft Dynamics Lifecycle Services (LCS) během počátečního nasazení nového tenanta elektronického obchodování.

## <a name="description"></a>popis

Když vytvoříte komponenty elektronického obchodování jako součást procesu nasazení nového tenanta elektronického obchodu, který zahrnuje komponentu Tvůrce webu Commerce, skupina zabezpečení Azure AD se v dialogovém okně nezobrazí jako možnost.

## <a name="resolution"></a>Rozlišení

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>Zřízení uživatele webu elektronického obchodu ve správném tenantovi

1. Přejděte na [portál Azure](https://portal.azure.com/).
1. Pod tenantem, pro který byl zřízen projekt LCS pro váš web elektronického obchodování, postupujte podle pokynů v části [Vytvoření základní skupiny a přidání členů pomocí Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Přejděte do [LCS](https://lcs.dynamics.com/) a přihlaste se pomocí účtu, který sdílí stejného tenanta jako skupina zabezpečení Azure AD, kterou jste právě vytvořili. Účet musí mít přístup k prohlížení skupiny zabezpečení Azure AD.
1. Proveďte kroky nastavení a nakonfigurujte web elektronického obchodování. Když zřídíte komponenty elektronického obchodování, skupina zabezpečení by se nyní měla zobrazit jako možnost v dialogovém okně.

> [!NOTE]
> Chcete-li zajistit, aby bylo pole v dialogovém okně vyplněno seznamem skupin zabezpečení, musíte vybrat **Enter** poté, co zadáte název skupiny zabezpečení Azure AD, kterou jste vytvořili. Výsledky hledání zobrazí seznam všech skupin zabezpečení Azure AD, které začínají hledaným textem a ke kterým má uživatel přístup. Můžete použít kratší hledaný výraz, abyste získali širší výsledky vyhledávání.

## <a name="additional-resources"></a>Další prostředky

[Vytvoření základní skupiny a přidání členů pomocí Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Nasazení nového klienta elektronického obchodu](../deploy-ecommerce-site.md)