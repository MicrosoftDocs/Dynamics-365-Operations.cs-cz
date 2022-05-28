---
title: Vytvoření platby DPH
description: Procedura úlohy Vyrovnat a zaúčtovat DPH slouží k vyrovnání zůstatků DPH na účtech DPH a jejich vyrovnání na účtu pro vyrovnání DPH za dané období.
author: twheeloc
ms.date: 01/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c388a8f98cd4581abe2ec13d8922e232321e4039
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735929"
---
# <a name="create-a-sales-tax-payment"></a>Vytvoření platby DPH

[!include [banner](../../includes/banner.md)]

Procedura úlohy Vyrovnat a zaúčtovat DPH slouží k vyrovnání zůstatků DPH na účtech DPH a jejich vyrovnání na účtu pro vyrovnání DPH za dané období.

1. Přejděte na **Daň > Přiznání > DPH > Vyrovnat a zaúčtovat DPH**.
2. V poli **Období vyrovnání** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Do pole **Od data** zadejte datum. Není-li vybrána možnost **Zahrnout opravy** na stránce **Parametry hlavní knihy**, vyrovnání lze zpracovat pro různé verze. **Na začátku** je první vyrovnání pro interval období, které lze zpracovat pouze jednou pro interval období. Nejnovější opravy vyrovnají transakce DPH, které byly zaúčtovány po vytvoření původní verze.
5. Zadejte datum do pole **Datum transakce**.
6. Vyberte **OK**. Sestava **Platby daně z prodeje** je vytištěna, aby bylo možné zkontrolovat vypořádané transakce daně z obratu v daném období.

Od verze Finance 10.0.24 můžete pomocí funkce **Oddělit generování hlášení o platbě daně z prodeje** v pracovním prostoru **Správa funkcí** vynechat generování sestavy po provedení postupu **Oddělit generování sestavy platby DPH** od vypořádání DPH v pracovním prostoru **Správa funkcí**.

Když je tato funkce povolena, po dokončení procesu vypořádání se nevytiskne žádná zpráva o zaplacení daně z obratu. Místo toho se zobrazí následující zpráva: „Vyúčtování a zaúčtování daně z obratu je dokončeno. Poukaz 'xxxx, m/d/yyyy' byl odeslán."

Přehled o platbě daně z prodeje můžete stále spustit ručně takto: **Daň** > **Dotazy a sestavy** > **Dotazy na DPH** > **Platby DPH**.

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
