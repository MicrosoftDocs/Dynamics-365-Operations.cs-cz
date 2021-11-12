---
title: Vytvoření platby DPH
description: Procedura úlohy Vyrovnat a zaúčtovat DPH slouží k vyrovnání zůstatků DPH na účtech DPH a jejich vyrovnání na účtu pro vyrovnání DPH za dané období.
author: twheeloc
ms.date: 10/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54132ca4775482b4a06ff7e73125e804aff40cb4
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700106"
---
# <a name="create-a-sales-tax-payment"></a>Vytvoření platby DPH

[!include [banner](../../includes/banner.md)]

Procedura úlohy Vyrovnat a zaúčtovat DPH slouží k vyrovnání zůstatků DPH na účtech DPH a jejich vyrovnání na účtu pro vyrovnání DPH za dané období.

1. Přejděte na **Daň > Přiznání > DPH > Vyrovnat a zaúčtovat DPH**.
2. V poli **Období vyrovnání** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Do pole **Od data** zadejte datum.
    - Není-li vybrána možnost **Zahrnout opravy** na stránce **Parametry hlavní knihy**, vyrovnání lze zpracovat pro různé verze. Na začátku je první vyrovnání pro interval období, které lze zpracovat pouze jednou pro interval období. Nejnovější opravy vyrovnají transakce DPH, které byly zaúčtovány po vytvoření původní verze.
5. Zadejte datum do pole **Datum transakce**.
6. Klikněte na tlačítko **OK**.

## <a name="performance-consideration"></a>Aspekty výkonnosti

Dokončení procesu platby DPH obratu může trvat dlouho. Hlavními faktory, které ovlivňují provedení postupu, jsou počet faktur v zúčtovacím období a počet záznamů, které musí být zaúčtovány na dokladu o vyúčtování DPH. Chcete-li zlepšit výkon, můžete se rozhodnout obejít některé funkce, které ve vašem procesu nejsou vyžadovány.

### <a name="enable-the-sales-tax-payment-performance-improvement-feature"></a>Aktivace funkce zlepšení výkonu plateb DPH

Funkce **Zlepšení výkonu platby DPH** může pomoci zlepšit výkon procesu platby DPH agregací částky v účetní měně a částky v měně vykazování na řádcích dokladu o platbě DPH, které mají stejný hlavní účet, dimenzi hlavní knihy a měnu, na jeden řádek.

1. Přejděte do nabídky **Správa systému** \> **Pracovní prostory** \> **Správa funkcí**.
2. Na kartě **Vše** vyhledejte a vyberte **Zlepšení výkonu platby daně z obratu**.
3. Vyberte **Povolit**.

### <a name="prevent-generation-of-offset-tax-transactions"></a>Zabránění vytváření kompenzovaných daňových transakcí

Ve výchozím nastavení doklad o zaplacení DPH obratu účtuje kompenzované transakce DPH proti každé transakci DPH, která je vypořádána v procesu platby DPH. Tyto kompenzované transakce DPH jsou zahrnuty do sestavy **Odsouhlasení DPH / hlavní knihy**. Zobrazují nevyrovnaný zůstatek transakcí DPH, které nebyly během období vypořádány.

Kompenzované transakce DPH však mohou zvýšit zátěž na postup placení DPH. Proto lze na vyžádání aktivovat testování, které se jmenuje **TaxReportGenOffsetTaxTransPerRecordSetFlighting**. Toto rozdělení může pomoci zlepšit výkon generování kompenzovaných daňových transakcí pro země a oblasti kromě Thajska, Polska, Maďarska, Litvy, Malajsie, Indie, Itálie, Ruska, Česka, Estonska a Lotyšska.

> [!NOTE]
> Pokud jsou v tabulce daňových transakcí přizpůsobená pole, nelze aktivovat rozdělení na období.

Protože sestava **Odsouhlasení DPH / hlavní knihy** se obecně používá pouze pro účely vnitřní kontroly a není vyžadována v mnoha daňových režimech, můžete se rozhodnout, že nebudete generovat kompenzované transakce DPH na dokladu o zaplacení DPH.

1. Přejděte na **Daň** \> **Nepřímé daně** \> **DPH** \> **Období vyrovnání DPH**.
2. Vyberte období vyrovnání.
3. Na pevné záložce **Všeobecné** nastavte možnost **Zabránit vytváření kompenzovaných daňových transakcí** na **Ano**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
