---
title: Konfigurace prostředí vyhodnocení Dynamics 365 Commerce
description: Toto téma vysvětluje, jak konfigurovat prostředí vyhodnocení Microsoft Dynamics 365 Commerce poté, co je zřízeno.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599717"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Konfigurace prostředí vyhodnocení Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Toto téma vysvětluje, jak konfigurovat prostředí vyhodnocení Microsoft Dynamics 365 Commerce poté, co je zřízeno.

## <a name="overview"></a>Přehled

Postupy v tomto tématu dokončete až po zřízení prostředí vyhodnocení Commerce. Informace o postupu zřízení prostředí vyhodnocení Commerce najdete v části [Zřízení prostředí vyhodnocení Commerce](provisioning-guide.md).

Po kompletním zřízení prostředí vyhodnocení Commerce je nutné dokončit další kroky konfigurace po zřízení, aby bylo možné začít posuzovat prostředí. K dokončení těchto kroků je nutné použít prostředí Lifecycle Services (LCS) Microsoft Dynamics a Dynamics 365 Commerce.

## <a name="before-you-start"></a>Než začnete

1. Přihlaste se do [portálu LCS](https://lcs.dynamics.com).
1. Přejděte na svůj projekt.
1. V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.
1. V seznamu vyberte své prostředí.
1. V informacích o prostředí vpravo vyberte **Přihlášení k prostředí**. Budete posláni do centrály Commerce.
1. Ujistěte se, že je v pravém horním rohu vybrána právnická osoba **USRT**.

Během činností po zřízení v centrále Commerce se ujistěte, že právnická osoba **USRT** je vždy vybrána.

## <a name="configure-the-point-of-sale"></a>Konfigurace pokladního místa

### <a name="associate-a-worker-with-your-identity"></a>Přidružení pracovníka k vaší identitě

Chcete-li pracovníka s vaší identitou přidružit, postupujte následovně v centrále Commerce.

1. Pomocí nabídky vlevo přejděte na **Moduly \> Retail and commerce \> Zaměstnanci \> Pracovníci**.
1. V seznamu vyhledejte a vyberte následující záznam: **000713 - Andrew Collette**.
1. V podokně akcí klikněte na možnost **Commerce**.
1. Vyberte **Stávající identita přidružení**.
1. Do pole **E-mail** vpravo od **Hledání pomocí e-mailu** zadejte svou e-mailovou adresu.
1. Vyberte **Vyhledat**.
1. Vyberte záznam obsahující vaše jméno.
1. Vyberte **OK**.
1. Zvolte **Uložit**.

### <a name="activate-cloud-pos"></a>Aktivovat Cloud POS

Chcete-li aktivovat Cloud POS, postupujte následovně v LCS.

1. V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.
1. V seznamu vyberte své prostředí.
1. V informacích o prostředí vpravo vyberte **Přihlášení ke cloudovému pokladnímu místu**.
1. Vyberte **Další**, chcete-li otevřít dialogové okno **Než začneš**.
1. Nechte pole **Adresa URL serveru** tak, jak je. Zvolte **Další**.
1. Přihlaste se pomocí účtu Microsoft Azure Active Directory (Azure AD).
1. Pro **Jméno obchodu** vyberte **San Francisco** a poté vyberte **Další**.
1. V **Registr a zařízení** vyberte **SANFRAN-1**.
1. Vyberte **Aktivovat**. Jste přihlášeni a přesměrováni na přihlašovací stránku POS.
1. Nyní se můžete přihlásit ke cloudovému POS pomocí ID operátora **000713** a hesla **123**.

## <a name="set-up-your-site-in-commerce"></a>Nastavení webu v Commerce

Pokud chcete začít nastavovat web vyhodnocení v Commerce, postupujte následovně.

1. Přihlaste se k nástroji pro tvorbu webu pomocí adresy URL, kterou jste si poznamenali při inicializaci e-Commerce během zřizování (viz [Inicializace e-Commerce](provisioning-guide.md#initialize-e-commerce)).
1. Vyberte web **Fabrikam** otevřete dialogové okno nastavení webu.
1. Vyberte doménu, kterou jste zadali při inicializaci platformy e-Commerce.
1. Jako výchozí kanál vyberte **Rozšířený online obchod společnosti Fabrikam**. (Zkontrolujte, zda jste vybrali **rozšířený** online obchod.)
1. Jako výchozí jazyk vyberte **en-us**.
1. Ponechte hodnotu pole **Cesta** tak, jak je.
1. Vyberte **OK**. Zobrazí se seznam stránek na webu.

## <a name="enable-jobs"></a>Povolit úlohy

Pokud chcete povolit úlohy v Commerce, postupujte takto:

1. Přihlaste se k prostředí (HQ).
1. Pomocí nabídky vlevo přejděte na **Retail and commerce \> Dotazy a sestavy \> Dávkové úlohy**.

    Zbývající kroky tohoto postupu musí být dokončeny pro každou z následujících úloh:

    * Zpracovat maloobchodní oznámení objednávky e-mailem
    * Dostupnost produktu
    * P-0001
    * Synchronizovat úlohu objednávek

1. Pomocí rychlého filtru vyhledejte úlohu podle názvu.
1. Je-li stav úlohy nastaven na **Probíhající**, postupujte následovně:

    1. Vybrat záznam.
    1. V podokně akcí na kartě **Dávková úloha** vyberte **Změnit stav**.
    1. Vyberte **Ruší se** a poté vyberte **OK**.

Volitelně můžete také nastavit interval opakování na jednu (1) minutu pro následující úlohy:

* Zpracovat úlohu maloobchodního oznámení objednávky e-mailem
* úloha P-0001
* Synchronizovat úlohu objednávek

### <a name="run-full-data-synchronization"></a>Spustit úplnou synchronizaci dat

Chcete-li spustit úplnou synchronizaci dat v Commerce, postupujte takto v centrále Commerce.

1. Pomocí nabídky vlevo přejděte na **Moduly \> Retail and commerce \> Nastavení centrály \> Plánovač velkoobchodu \> Databáze kanálů**.
1. Vyberte kanál, který je nazvaný **scXXXXXXXXX**.
1. V podokně akcí vyberte **Úplná synchronizace dat**.
1. Jako plán distribuce zadejte **9999**.
1. Vyberte **OK**.
1. Vyberte **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Testování informací o kreditní kartě za účelem provedení zkušebních nákupů

Chcete-li provést zkušební transakce na webu, můžete použít následující testovací kreditní kartu:

- **Číslo karty:** 4111-1111-1111-1111
- **Datum konce platnosti:** 10/20
- **Ověřovací hodnota platební karty (CVV):** 737

> [!IMPORTANT]
> V žádném případě byste neměli používat informace o skutečné kreditní kartě na testovacím webu.

## <a name="next-steps"></a>Další kroky

Po dokončení postupu zřizování a konfigurace můžete začít používat prostředí vyhodnocení. Pomocí adresy URL nástroje pro tvorbu webu Commerce můžete přejít na práci s vytvářením. Pomocí adresy URL webu Commerce přejděte do prostředí webu zákazníka maloobchodu.

Pokud chcete provést konfiguraci volitelných funkcí prostředí vyhodnocení Commerce, najdete informace v části [konfigurace volitelných funkcí prostředí vyhodnocení Commerce](cpe-optional-features.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled prostředí vyhodnocení Dynamics 365 Commerce](cpe-overview.md)

[Zřízení prostředí vyhodnocení Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce](cpe-optional-features.md)

[Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce](cpe-bopis.md)

[Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Portál Microsoft Azure](https://azure.microsoft.com/features/azure-portal)

[Web Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)
