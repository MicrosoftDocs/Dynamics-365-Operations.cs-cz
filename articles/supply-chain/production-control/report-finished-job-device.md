---
title: Ohlášení jako dokončené ze zařízení úkolového lístku
description: Toto téma popisuje, jak nakonfigurovat systém tak, aby uživatelé zařízení úkolového lístku mohli vykazovat hotové produkty z výrobní zakázky do zásob.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403255"
---
# <a name="report-as-finished-from-the-job-card-device"></a>Ohlášení jako dokončené ze zařízení úkolového lístku

[!include [banner](../includes/banner.md)]

Pracovníci používají stránku **Zpráva o pokroku** v zařízení úkolového lístku k vykazování množství, která byla dokončena pro výrobní úlohu.

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a>Kontrola, zda jsou do zásob přidána množství, která jsou hlášena jako hotová

Chcete-li určit, zda a jak se mají do zásob přidávat množství, která jsou hlášena jako hotová při poslední operaci, postupujte takto.

1. Klikněte na **Řízení výroby \> Nastavení \> Provádění výroby \> Výchozí hodnoty výrobní zakázky**.
1. Na kartě **Vykázat jako hotové** nastavte pole **Aktualizovat hlášení o dokončených online** na některou z následujících hodnot:

    - **Ne** - Při vykazování množství při poslední operaci nebude do zásob přidáno žádné množství. Stav výrobního příkazu se ale nezmění nikdy.
    - **Stav + množství** - Stav výrobního příkazu se změní na *Hlášeno jako dokončené* a množství v zásobách bude hlášeno jako dokončené.
    - **Množství** - Množství bude hlášeno jako hotové ve skladu, ale stav výrobního příkazu se nikdy nezmění.
    - **Stav** Změní se pouze stav výrobního příkazu. Při vykazování množství při poslední operaci nebude do zásob přidáno žádné množství.

> [!NOTE]
> Množství není sledováno v zásobách, pokud operace, které jsou hlášeny jako dokončené, nejsou definovány jako poslední operace. Tato množství však lze použít k zobrazení pokroku. Mohou být také zahrnuta do pravidel, která určují, zda pracovníci mohou zahájit další operaci před dosažením definovaného prahu vykazovaných množství při předchozí operaci. Tato pravidla můžete definovat na kartě **Ověření množství** stránky **Výchozí hodnoty výrobního příkazu**.

Více informací o tom, jak pracovat se stránkou **Výchozí hodnoty výrobního příkazu** uvádí téma [Parametry výroby v realizaci výroby](production-parameters-manufacturing-execution.md).

## <a name="report-batch-controlled-items-as-finished"></a>Hlášení dávek kontrolovaných položek jako dokončených

Zařízení úkolového lístku podporuje tři scénáře pro vykazování položek dávek. Tyto scénáře platí jak pro položky, které jsou povoleny pro pokročilé skladové procesy, tak pro položky, které nejsou povoleny pro pokročilé skladové procesy.

- **Ručně přiřazená čísla dávek:** Pracovníci zadají vlastní číslo dávky. Toto číslo dávky může pocházet z externího zdroje, který systém nezná.
- **Předdefinovaná čísla dávek:** Pracovníci vyberou číslo dávky ze seznamu čísel dávek, které systém automaticky vygeneruje před uvolněním výrobního příkazu do zařízení úkolového lístku.
- **Opravená čísla dávek:** Pracovníci nezadají ani nevyberou číslo dávky. Místo toho systém automaticky přiřadí číslo dávky pracovnímu příkazu před vydáním.

Pokud chcete jednotlivé scénáře povolit, postupujte následovně.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte produkt ke konfiguraci.
1. Na pevné záložce **Správa zásob** v poli **Skupina čísel dávek** vyberte skupinu čísla sledování, která je nastavená na podporu vašeho scénáře.

> [!NOTE]
> Pokud není ve výchozím nastavení číslu kontrolovanému podle dávek přiřazená žádná skupina čísel dávek, poskytne zařízení úkolového lístku ruční zadání čísla dávky během vykazování jako dokončené.

Následující podkapitoly popisují, jak nastavit skupiny sledovacích čísel na podporu každého ze tří scénářů pro vykazování položek dávek.

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a>Povolení vykazování čísel dávek v zařízení úkolového lístku

Chcete-li povolit, aby vaše zařízení úkolového lístku přijímala číslo dávky během hlášení jako dokončené, musíte použít [správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) k zapnutí následujících funkcí (v tomto pořadí):

1. Vylepšené uživatelské prostředí pro dialogové okno průběhu sestavy v zařízení úkolového lístku
1. Umožňuje zadávat čísla dávky a sériová čísla při vykazování za dokončené v zařízení úkolového lístku (Preview)

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>Nastavení skupiny čísel sledování, která pracovníkům umožňuje ruční přiřazení čísla dávky

Při nastavení skupiny čísel tak, aby vyžadovalo od pracovníků ruční přiřazení čísel dávek, postupujte následovně.

1. Přejděte na **Správa zásob \> Nastavení \> Dimenze \> Skupiny čísel sledování**.
1. Vytvořte nebo vyberte skupinu sledovacích čísel, kterou chcete nastavit.
1. Na pevné záložce **Obecné** nastavte možnost **Ruční** na **Ano**.

    ![Stránka skupin sledovacích čísel](media/tracking-number-group-manual.png "Stránka skupin sledovacích čísel")

1. Nastavte další hodnoty podle potřeby a poté vyberte tuto skupinu sledovacích čísel jako skupinu čísel dávek vydaných produktů, pro které chcete tento scénář použít.

Při použití tohoto scénáře pole **Číslo dávky**, které poskytuje stránka **Nahlásit pokrok** na kartě zařízení úkolového lístku, poskytuje textové pole, do něhož mohou pracovníci zadat libovolnou hodnotu.

![Stránka hlášení pokroku s polem pro ruční čísla dávky](media/job-card-device-batch-manual.png "Stránka hlášení pokroku s polem pro ruční čísla dávky")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>Nastavte skupinu sledovacích čísel, která poskytuje seznam předdefinovaných čísel dávky

Pokud chcete poskytnout seznam předdefinovaných čísel dávky, nastavte skupinu sledovacích čísel následovně.

1. Přejděte na **Správa zásob \> Nastavení > Dimenze \> Skupiny čísel sledování**.
1. Vytvořte nebo vyberte skupinu sledovacích čísel, kterou chcete nastavit.
1. Na pevné záložce **Obecné** nastavte možnost **Pouze pro transakce zásob** na **Ano**.
1. Pomocí pole **Na množství** rozdělte čísla dávky na množství na základě zadané hodnoty. Například máte výrobní zakázku na deset kusů a v poli **Na množství** je nastavena hodnota *2*. V takovém případě bude výrobní zakázce při vytvoření přiřazeno pět čísel dávky.

    ![Stránka skupin sledovacích čísel](media/tracking-number-group-predefined.png "Stránka skupin sledovacích čísel")

1. Nastavte další hodnoty podle potřeby a poté vyberte tuto skupinu sledovacích čísel jako skupinu čísel dávek vydaných produktů, pro které chcete tento scénář použít.

Při použití tohoto scénáře pole **Číslo dávky**, které poskytuje stránka **Nahlásit pokrok** na zařízení úkolového lístku, představuje rozevírací seznam, kde pracovníci musí vybrat předdefinovanou hodnotu.

![Stránka hlášení pokroku se seznamem předdefinovaných čísel dávky](media/job-card-device-batch-predefined.png "Stránka hlášení pokroku se seznamem předdefinovaných čísel dávky")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>Nastavení skupiny čísel sledování, která automaticky přiřazuje čísla dávky

Pokud mají být čísla dávky přidělována automaticky beze vstupu pracovníka, nastavte skupinu čísel sledování podle následujících kroků.

1. Přejděte na **Správa zásob \> Nastavení \> Dimenze \> Skupiny čísel sledování**.
1. Vytvořte nebo vyberte skupinu sledovacích čísel, kterou chcete nastavit.
1. Na pevné záložce **Obecné** nastavte možnost **Pouze pro transakce zásob** na **Ne**.
1. Nastavte možnost **Ruční** na **Ne**.

    ![Stránka skupin sledovacích čísel](media/tracking-number-group-fixed.png "Stránka skupin sledovacích čísel")

1. Nastavte další hodnoty podle potřeby a poté vyberte tuto skupinu sledovacích čísel jako skupinu čísel dávek vydaných produktů, pro které chcete tento scénář použít.

Při použití tohoto scénáře pole **Číslo dávky**, které poskytuje stránka **Nahlásit pokrok** na kartě zařízení úkolového lístku, zobrazuje hodnotu, kterou však pracovníci nemohou upravovat.

![Stránka hlášení pokroku s polem pro pevná čísla dávky](media/job-card-device-batch-fixed.png "Stránka hlášení pokroku s polem pro pevná čísla dávky")

## <a name="report-as-finished-to-a-license-plate"></a>Nahlášení jako dokončené do registrační značky

Pokročilé skladové procesy mohou pomocí rozměru registrační značky sledovat zásoby ve skladovacích místech, která byla pro tento účel nastavena. V tomto případě je registrační značka vyžadována, když pracovník nahlásí množství jako dokončená.

### <a name="enable-license-plate-reporting-and-label-printing"></a>Povolení vykazování registrační značky a tisku štítku

Chcete-li používat funkce popsané v této části, musíte použít [správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) pro zapnutí následujících funkcí (v tomto pořadí):

1. Registrační značka pro vykazování jako dokončené přidána do zařízení úkolového lístku
1. Povolit automatické generování čísla registrační značky při vykazování jako dokončeno v zařízení úkolového lístku
1. Vytisknout štítek ze zařízení úkolového lístku

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a>Nastavení hlášení jako dokončené do registrační značky

Chcete-li určit, zda by pracovníci měli znovu použít existující registrační značku nebo vygenerovat novou registrační značku, když ohlásí množství jako dokončené, postupujte následovně.

1. Přejděte do nabídky **Řízení výroby \> Nastavení \> Provádění výroby \> Konfigurovat úkolový lístek pro zařízení**.
2. U každého zařízení nastavte následující možnosti:

    - **Generovat registrační značku** – Nastavením této možnosti na **Ano** vygenerujete novou registrační značku pro každé nahlášení jako dokončené. Nastavte ji na **Ne**, pokud by se pro každé hlášení měla použít stávající registrační značka.
    - **Tisk štítku** – Nastavte tuto možnost na **Ano**, pokud pracovník musí vytisknout registrační značku pro každé hlášení jako dokončené. Nastavte ji na **Ne**, pokud není vyžadován žádný popisek. 

![Stránka Konfigurovat úkolový lístek pro zařízení](media/config-job-card-raf.png "Stránka Konfigurovat úkolový lístek pro zařízení")

> [!NOTE]
> Pokud chcete konfigurovat štítek, přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Směrování dokumentu**. Další informace získáte v části [Povolení tisku štítků registračních značek](../warehousing/tasks/license-plate-label-printing.md).
