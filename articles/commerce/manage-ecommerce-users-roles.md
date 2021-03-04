---
title: Správa uživatelů e-Commerce a rolí
description: V tomto tématu je vysvětleno, jak udělit uživatelům přístup k vývojovému prostředí vašeho webu Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a1f9abae20d0f2e71790a3b27337338dc042b52
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410671"
---
# <a name="manage-e-commerce-users-and-roles"></a>Správa uživatelů e-Commerce a rolí


[!include [banner](includes/banner.md)]

V tomto tématu je vysvětleno, jak udělit uživatelům přístup k vývojovému prostředí vašeho webu Microsoft Dynamics 365 Commerce.

Chcete-li pomoci řídit uživatelský přístup a udělit uživatelům oprávnění k provádění konkrétních úkolů, používá vývojové prostředí na webu skupiny zabezpečení, které vytvoříte v Microsoft Azure Active Directory (Azure AD). Nejprve přiřaďte novou nebo existující skupinu zabezpečení z Azure AD k jednotlivým rolím ve vývojovém prostředí. Poté přiřadíte nebo odvoláte oprávnění pro jednotlivé uživatele tím, že přidáte tyto uživatele do příslušné skupiny zabezpečení nebo je odeberete ze skupiny zabezpečení.

## <a name="overview-of-roles-in-the-authoring-environment"></a>Přehled rolí ve vývojovém prostředí

Vývojové prostředí Dynamics 365 for Commerce podporuje následující role.

| Role                 | Popis |
|----------------------|-------------|
| Správce systému | Uživatelé s touto rolí mají všechna oprávnění pro všechny nástroje a pro všechna hodnocení a recenze. Mohou také vytvářet weby. |
| Správce   | Uživatelé s touto rolí mají všechna oprávnění pro všechny nástroje a RnR v dané struktuře webu. |
| Webový výrobce         | Uživatelé s touto rolí mohou vytvářet stránky, fragmenty a šablony, odesílat a spravovat aktiva a obohacovat produkty a kategorie. |
| Prohlížeč               | Uživatelé s touto rolí mohou zobrazit stránky, šablony, aktiva, fragmenty, rozvržení a nastavení, ale nesmí provádět žádné změny. |
| Moderátor RnR        | Uživatelé s touto rolí mohou moderovat recenzování produktů. |

## <a name="system-administrator-role"></a>Role Správce systému

Pokud zřizujete Dynamics 365 Commerce v prostředí služby Microsoft Dynamics Lifecycle Services (LCS), budete požádáni o poskytnutí skupiny zabezpečení pro roli **Správce systému**. Tato role se poté automaticky použije na všechny weby, které vytvoříte v prostředí, které konfigurujete. Skupinu zabezpečení pro tuto roli lze aktualizovat pouze v rámci LCS. Na stránce **Správa webu** pro všechny weby se zobrazí pouze pro čtení a slouží pouze k informačním účelům.

## <a name="administrator-role"></a>Role správce

Při vytváření nového webu v rámci Commerce budete požádáni o poskytnutí skupiny zabezpečení pro roli **Správce**. Přehled oprávnění, která tato role uděluje, naleznete v tabulce uvedené výše v tomto tématu.

## <a name="add-or-update-security-groups"></a>Přidat nebo aktualizovat skupiny zabezpečení

Po vytvoření webu mohou k vývojovému prostředí daného webu přistupovat pouze uživatelé, kteří jsou ve skupinách zabezpečení a mají role **Správce systému** a **Správce**. Chcete-li přiřadit uživatele k rolím **Tvůrce webu**, **Moderátor RnR** a **Prohlížeč**, je nutné těmto rolím přiřadit skupiny zabezpečení. Chcete-li přidat skupinu zabezpečení do role nebo aktualizovat skupinu zabezpečení, která je aktuálně přiřazena k roli, postupujte podle následujících kroků.

1. Přejděte na web, který chcete aktualizovat.
1. V **Správě webu** otevřete stránku **Zabezpečení**.
1. Vyberte roli, kterou chcete upravit.
1. Přidejte skupiny zabezpečení k rolím nebo odeberte skupiny zabezpečení z rolí.

## <a name="additional-resources"></a>Další zdroje

[Přidání kódu skriptu na webové stránky pro podporu telemetrie](add-telemetry.md)

[Zvažování optimalizace webového vyhledávače pro váš web](search-engine-optimization-considerations.md)

[Správa zásad zabezpečení obsahu (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]