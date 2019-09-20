---
title: Kontrola pracovní doby
description: Tohle téma popisuje kontrolu pracovní doby v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 916e7b8d5d494dbae0659504957f7f0798a6834b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918365"
---
# <a name="work-hour-control"></a>Kontrola pracovní doby

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

V modulu Správa majetku můžete vypočítat počet hodin pro získání přehledu o skutečných hodinách ve srovnání s rozpočtovými hodinami na majetku, funkčních místech nebo pracovních příkazech. Skutečné hodiny jsou založeny na zaúčtovaných transakcích.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>Řízení pracovní doby pro majetek, funkční místa a pracovní příkazy

Výpočty vytvořené pro majetek, funkční místa a pracovní příkazy jsou téměř totožné. Jediný rozdíl je to, že pro majetek a funkční místa lze do výpočtu zahrnout i dílčí majetek a dílčí skladová místa. Datum je datum transakce, kdy byla zaznamenána registrace.

1. Klepněte na položku **Správa majetku** > **Dotazy** > **Majetek** > **Řízení hodin majetku** nebo **Řízení hodin funkčního místa** nebo **Správa majetku** > **Dotazy** > **pracovní příkazy** > **Řízení hodin na pracovního příkazu**.

2. V dialogovém okně **Řízení hodin majetku**.

3. V dialogovém okně **Řízení hodin majetku** / **Řízení hodin funkčního místa** / **Řízení hodin pracovního příkazu** vyberte období, které má být vypočteno v polích **Od data** a **Do data**.

4. V případě potřeby vyberte **Sadu finančních dimenzí**, která má být zahrnuta do výpočtu.

5. Nechcete-li zobrazit výsledky obsahující nula hodin, vyberte možnost Ano na přepínacím tlačítku **Přeskočit nulu**.

6. V poli **Úroveň** určete, jak detailní mají být řádky řízení hodin v případě funkčních míst. Pokud například do pole zadáte číslo „1“ a máte hierarchii funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky řízení hodin pro funkční místo, a proto lze navýšit hodiny na řádku z funkčních míst na nižší úrovni. Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky řízení hodin na všech úrovních funkčních míst, ke kterým se vztahují.

7. Chcete-li zobrazit náklady související s dílčími aktivy jako samostatné řádky, vyberte možnost Ano na přepínacím tlačítku **Zahrnout dílčí aktiva**.

8. Chcete-li hledání omezit, můžete vybrat konkrétní majetek/funkční skladová místa/pracovní příkazy na pevné záložce **Záznamy, které mají být zahrnuty**.

9. Výpočet zahájíte klepnutím na tlačítko **OK**.

10. Na stránce **Řízení hodin majetku**, ve skupinách podokna akce **Seskupit podle...** vyberte odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu. Vybraná tlačítka podokna akcí jsou zvýrazněna. Kliknutím na tlačítko jej aktivujte nebo deaktivujte.

Následující obrázek ukazuje příklad výpočtu **Řízení hodin majetku**.

![Obrázek č. 1](media/04-controlling-and-reporting.png)

Dalším způsobem provedení výpočtu hodin je vybrat více majetku v možnosti **Všechen majetek** nebo **Aktivní majetek**. Poté klikněte na tlačítko **Řízení hodin** na pevné záložce **Obecné**. Vybraný majetek je automaticky vložen do pole **Majetek** na pevné záložce **Záznamy, které mají být zahrnuty**. Klikněte na tlačítko **OK** v dialogovém okně **Řízení hodin majetku** a zobrazí se výpočet pro vybraný majetek. Stejný postup lze provést pro funkční místa ve volbě **Všechna funkční místa** nebo **Aktivní funkční místa** a pro pracovní příkazy ve volbě **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

>[!NOTE]
>V poli **Původní rozpočet** jsou uvedeny rozpočtové hodiny z prognózy pracovního příkazu. Pole **Skutečné hodiny** zobrazuje zaúčtované hodiny na pracovních příkazech. Pole **Potvrzené hodiny** zobrazuje celkové množství hodin, které vaše společnost potvrdila ve vztahu k pracovním příkazům.
