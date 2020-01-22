---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (10. prosince 2019)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b4bb599be27e7d97fed1c060f97627c7c6a868e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915503"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (10. prosince 2019)

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2660. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Pracovní prostor Správa funkcí

Pracovní prostor **Správa funkcí** uvádí seznam funkcí dodaných v jednotlivých vydáních. Ve výchozím nastavení jsou nové funkce vypnuté. Pracovní prostor slouží k jejich zapnutí a zobrazení odpovídající dokumentace. Další informace o aktivaci správy funkcí naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Všechny nové funkce zůstanou v náhledu nejméně 30 dnů a obvykle jsou zde 30-60 dní. Hlavní funkce jsou obvykle k dispozici v říjnu a dubnu každého roku po období náhledu. Jakmile se v pracovním prostoru **Správa funkcí** zobrazí nové funkce, můžete je zapnout. Některé funkce mohou být ve výchozím nastavení zapnuty.
 
V některých případech bude ve výchozím nastavení zapnuta integrální funkce a nelze ji vypnout (například pracovní prostor **Správa funkcí**).
 
Jakmile je funkce obecně k dispozici, může být zapnuta nebo vypnuta v provozních prostředích. Pracovní prostor **Správa funkcí** označuje, kdy bude funkce náhledu povinná. Toto datum je obvykle 1. října nebo 1. ledna, aby bylo možné vyrovnat je s pololetními plány vydávání. Nemůžete zapínat a vypínat povinné funkce. Dokud nebude povinná, můžete funkci zapnout nebo vypnout ve všech prostředích.

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>Zjednodušený pracovní formulář byl přesunut do pracovního prostoru správy funkcí (390583).

Pomocí této změny lze nyní povolit efektivnější pracovní formulář v pracovním prostoru **Správa funkcí**. Tato funkce byla přesunuta z formuláře **Systémové parametry** ve **Správě systému**.

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>Zabránění zápisu záznamů HcmWorkerPayrollInfo bez hodnoty pracovníka (394526)

V této verzi již nejsou v tomto scénáři vytvářeny záznamy **hcmworkerpayrollinfo** bez odkazu na pracovníka. 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>Protokol zpráv přidružený k akci není naplněn, pokud akce nebude dokončena (374007)

Tato verze obsahuje změnu, která naplní protokol hlášení akce v případě selhání akce v určitých scénářích. 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>Tvorba dávkové úlohy integrace Common data service (388030)

Při této změně jsou dávkové úlohy pro integraci Common Data Service vytvářeny, když je služba povolena.

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Další hodnoty seznamu výdeje ve vlastních polích se neodrazí v Common Data Service po kliknutí na tlačítko Použít ve formuláři vlastních polí (379599)

Při této změně jsou nyní nové hodnoty seznamu vyskladnění zadané v Talentu synchronizovány s Common Data Service při použití změn.

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>Aktualizace na Common Data Service a ponechání bankovní entity transakce se změní na vložku na straně Talent (352938)

Tato změna opravuje problém, kdy aktualizace na operaci odchodu do banky vytvoří nový záznam v Talentu.

## <a name="in-preview"></a>Náhled

Funkce náhledu jsou k dispozici pouze v prostředích **Sandbox**.

### <a name="print-performance-reviews"></a>Tisk kontrol výkonnosti

Viz [Tisk shrnutí výkonu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) v plánu Dynamics 365: 2019 release wave 2.

