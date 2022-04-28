---
title: Prázdný seznam daňových funkcí v parametrech výpočtu daně
description: Toto téma vysvětluje, jak řešit problém, kdy je seznam funkcí daně na stránce Parametry výpočtu daně prázdný.
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: ef8158c2ada18e7d132eebbedef559b3f80ab19f
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612282"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>Prázdný seznam daňových funkcí v parametrech výpočtu daně

[!include [banner](../includes/banner.md)]


## <a name="symptom"></a>Příznak

Publikovali jste funkci ve službě Regulatory Configuration Service (RCS), abyste ji mohli používat v Microsoft Dynamics 365 Finance. Když však otevřete Finance, přejdete na **Daň** \> **Nastavení** \> **Konfigurace daně** \> **Parametry výpočtu daně** a zkusíte vybrat hodnotu v poli **Název nastavení funkce**, seznam hodnot je prázdný.

## <a name="reason"></a>Důvod

K tomuto problému obvykle dochází, protože vaše prostředí Finance a prostředí RCS nejsou pod stejným tenantem.

### <a name="rcs-tenant"></a>Tenant RCS

Chcete-li zjistit ID svého tenanta RCS, postupujte podle těchto kroků.

1. Zkopírujte celou adresu URL RCS. Adresa URL může být například `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`.
2. Otevřete okno prohlížeče InPrivate, vložte adresu URL RCS do adresního řádku a poté vyberte **Enter**. Budete přesměrováni na přihlašovací stránku, kde najdete ID tenanta RCS. Pokud je například adresa URL přihlašovací stránky `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d`, ID tenanta je informace, která se objeví za `https://login.microsoftonline.com/`, tedy **d335a570-a05b-4bc5-8eb3-c42c65f9560d**.

### <a name="finance-environment-tenant-id"></a>ID tenanta prostředí Finance

Chcete-li najít ID tenanta pro vaše finanční prostředí, postupujte podle stejných kroků, které jste použili při hledání tenanta RCS. Místo úplné adresy URL RCS však zkopírujte a vložte celou adresu URL svého prostředí Finance.

## <a name="resolution"></a>Řešení

Pokud se dvě ID tenantů liší, narazíte na problém popsaný v tomto tématu. Pokud jsou stejné, narážíte na nesouvisející problém. V takovém případě doporučujeme kontaktovat podporu společnosti Microsoft.

### <a name="solution-1"></a>Řešení 1

Přihlaste své prostředí RCS ke stejnému tenantovi, ke kterému je přihlášeno vaše prostředí Finance. Poté vytvořte a publikujte daňový prvek.

### <a name="solution-2"></a>Řešení 2

Sdílejte daňovou funkci s finančním tenantem v RCS.

1. V RCS přejděte na **Funkce globalizace** \> **Výpočet daně**.
2. Vyberte funkci, kterou chcete sdílet, a poté na kartě **Organizace** vyberte **Sdílet s**.
3. Do pole **Název domény organizace** zadejte název. Například zadejte **contoso.onmicrosoft.com**.
4. Vyberte **Sdílet**.

![Sdílejte pomocí dialogového okna externí organizace.](media/ShareTaxFeature.png)
