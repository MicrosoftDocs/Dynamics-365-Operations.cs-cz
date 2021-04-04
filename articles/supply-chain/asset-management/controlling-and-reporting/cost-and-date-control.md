---
title: Kontrola data a nákladů
description: Toto téma popisuje kontrolu data a nákladů v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7072cb8c3f76be5869239aa0acab6cf3ff268e32
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253775"
---
# <a name="cost-and-date-control"></a>Kontrola data a nákladů

[!include [banner](../../includes/banner.md)]

 

V modulu Správa majetku můžete vypočítat náklady pro získání přehledu o skutečných nákladech ve srovnání s rozpočtovými náklady na majetku, funkčních místech a pracovních příkazech. Skutečné náklady jsou založeny na zaúčtovaných transakcích. 

Výpočet data lze provést také v případě, že chcete porovnat plánovaná počáteční a koncová data se skutečným počátečním a koncovým datem na pracovních příkazech.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Řízení nákadů pro majetek, funkční místa a pracovní příkazy

Výpočty vytvořené pro majetek, funkční místa a pracovní příkazy jsou téměř totožné. Jediný rozdíl je to, že pro majetek a funkční místa lze do výpočtu zahrnout i dílčí majetek a dílčí skladová místa. Datum je datum transakce, kdy byla zaznamenána registrace.

1. Klepněte na položku **Správa majetku** > **Dotazy** > **Majetek** > **Řízení nákladů majetku** nebo **Řízení v funkčního místa** nebo **Správa majetku** > **Dotazy** > **pracovní příkazy** > **Řízení nákladů pracovního příkazu**.

2. V dialogovém okně **Řízení nákladů majetku** / **Řízení nákladů funkčního místa** / **Řízení nákladů pracovního příkazu** vyberte časový rozsah, který má být vypočítán.

3. V případě potřeby vyberte sadu finančních dimenzí, která má být zahrnuta do výpočtu.

4. Nechcete-li zobrazit výsledky obsahující nulové náklady, vyberte možnost Ano na přepínacím tlačítku **Přeskočit nulu**.

5. V poli **Úroveň** určete, jak detailní mají být řádky řízení nákladů v případě funkčních míst. 

    Pokud například do pole zadáte číslo „1“ a máte hierarchii funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky řízení nákladů pro funkční místo, a proto lze navýšit hodiny na řádku z funkčních míst na nižší úrovni. 
    
    Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky řízení nákladů na všech úrovních funkčních míst, ke kterým se vztahují.

6. Chcete-li do výpočtu zahrnout tento sloupec, vyberte Ano na přepínači **Zobrazit otevřené potvrzené náklady**.

7. Chcete-li zobrazit náklady související s dílčími aktivy jako samostatné řádky, vyberte možnost Ano na přepínacím tlačítku **Zahrnout dílčí aktiva**.

8. Chcete-li hledání omezit, můžete vybrat konkrétní majetek/funkční skladová místa/pracovní příkazy na pevné záložce **Záznamy, které mají být zahrnuty**.

9. Výpočet zahájíte klepnutím na tlačítko **OK**.

    Následující obrázek ukazuje příklad dialogového okna **Řízení nákladů majetku**.

    ![Dialogové okno Řízení nákladů na majetek](media/01-controlling-and-reporting.png)

10. Na kartě **Kontrola nákladů majetku** klikněte na tlačítka **Seskupit podle** pro zobrazení požadované úrovně podrobností výpočtu. Vybraná tlačítka **Seskupit podle** jsou zvýrazněna. Kliknutím na tlačítko jej aktivujte nebo deaktivujte.

## <a name="example"></a>Příklad

Následující snímek obrazovky ukazuje příklad výpočtu výsledků v možnoti **Řízení nákladů majetku**.

- V poli **Původní rozpočet** jsou uvedeny rozpočtové náklady z prognózy pracovního příkazu. 
- Pole **Potvrzené náklady** zobrazí celkovu částku výdajů, které se právnická osoba zavázala platit. 
- Pole **Otevřené potvrzené náklady** zobrazuje závazky k zaplacení za položky, hodiny a služby, které byly objednány nebo přijaty, ale dosud nebyly zaplaceny. 
- Po zaúčtování všech registrací spotřeby budou související náklady zahrnuty do pole **Skutečné náklady**.

![Příklad výsledků výpočtu v řízení nákladů na majetek](media/02-controlling-and-reporting.png)

Dalším způsobem provedení výpočtu nákladů je vybrat více majetku v možnosti **Všechen majetek** nebo **Aktivní majetek**. Poté klikněte na tlačítko **Řízení nákladů** na kartě **Obecné**. V dialogovémokně  **Řízení nákladů majetku** je vybraný majetek automaticky vložen do pole **Majetek** na záložce s náhledem **Záznamy k zahrnutí**. Klikněte na **OK** a zobrazí se výpočet nákladů pro vybraný majetek. Stejný postup lze provést pro funkční místa ve volbě **Všechna funkční místa** nebo **Aktivní funkční místa** a pro pracovní příkazy ve volbě **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.


## <a name="work-order-date-control"></a>Řízení data pracovního příkazu

Na této stránce můžete získat přehled o očekávaných počátečních a koncových datech ve srovnání se skutečnými počátečními a koncovými daty na pracovních příkazech.

1. Klikněte na **Správa majetku** > **Dotazy** > **Pracovní příkazy** > **Kontrola data pracovního příkazu**.

2. Klikněte na tlačítko **Vypočítat.**

3. V poli **Funkční místo** zvolte funkční místo.

4. Vložte rozsah, pro který chcete provést výpočet v polích **Od data** a **Do data**. Budou zahrnuty všechny pracovní příkazy s očekávaným datem zahájení v daném rozsahu.

5. Klikněte na tlačítko **OK**.

6. Ve skupině **Seskupit podle** klikněte na odpovídající tlačítka pro zobrazení požadované úrovně podrobností výpočtu. Vybraná tlačítka **Seskupit podle** jsou zvýrazněna. Kliknutím na tlačítko jej aktivujte nebo deaktivujte.

## <a name="example"></a>Příklad

Následující snímek obrazovky ukazuje příklad výpočtu výsledků v možnoti **Kontrola data pracovního příkazu**.

- Pole **Průměrné zpoždění zahájení** zobrazuje rozdíl mezi dny plánovaného počátečního data pro pracovní příkaz ve srovnání se skutečným počátečním datem. Pokud například skutečné datum zahájení bylo dva dny před plánovaným počátečním datem, zobrazí se v tomto poli -2.  
- Pole **Průměrné zpoždění ukončení** zobrazuje rozdíl mezi dny plánovaného koncového data pro pracovní příkaz ve srovnání se skutečným koncovým datem. Pokud například skutečné datum ukončení bylo tři dny po plánovaném koncovém datu, zobrazí se v tomto poli 3.  
- V poli **Výskyty** se zobrazuje počet časových odchylek v závislosti na plánovaném a skutečném počátečním datu a plánovaném a skutečném koncovém datu na pracovním příkazu.

![Příklad výsledků výpočtu v řízení pracovních příkazů](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]