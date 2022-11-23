---
title: Snímky sledování splatnosti odběratele
description: Tento článek obsahuje informace o časových snímcích zákazníka. Snímek sledování splatnosti vypočítá časové zůstatky skupiny zákazníků v jednom bodu v čase.
author: JodiChristiansen
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: e4ccc8ac9b5374ca0713167a17b8704727c687fd
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775229"
---
# <a name="customer-aging-snapshots"></a>Snímky sledování splatnosti odběratele

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o časových snímcích zákazníka. Snímek sledování splatnosti vypočítá časové zůstatky skupiny zákazníků v jednom bodu v čase. Můžete vytvořit záznamy snímků sledování splatnosti buď pro všechny zákazníky nebo pro zákazníky ve fondu zákazníků.

Informace ze snímku sledování splatnosti se zobrazují na stránce se seznamem **Splatné zůstatky** a na stránce **Inkasa**. Je třeba snímek sledování splatnosti vytvořit před použitím stránky seznamu **Splatné zůstatky**. Na stránce se zobrazují informace pouze pro odběratele, pro které byl vytvořen snímek sledování splatnosti.

Pracovní prostor **Úvěr a kolekce zákazníků** také ukazuje sledování splatnosti zákazníka. Další informace viz [Správa úvěrů a inkas obsahu Power BI](credit-collections-power-bi.md).

> [!NOTE]
> Chcete-li zkrátit čas potřebný k vytvoření snímku sledování splatnosti, zapněte následující funkce v pracovním prostoru **Správa funkcí**: 
> - **Vylepšení výkonu prodlení odběratelů** 
> - **Zlepšení výkonu sledování splatnosti zákazníka pomocí fondů zákazníků**  
>Jsou-li aktivovány obě funkce, lze **Zákaznické skupiny** použít při vytváření snímku stárnutí. 

Když vytvoříte snímek sledování splatnosti, zadejte do něj následující pole:

- **Definice období pro sledování splatnosti** - vyberte definici období pro sledování splatnosti pro snímek sledování splatnosti. Lze nastavit jeden snímek sledování splatnosti pro každou definici období pro sledování splatnosti. Snímek sledování splatnosti a definice období pro sledování splatnosti musí být vytvořeny samostatně.
- **ID fondu** - Toto pole je volitelné. Pomocí fondu můžete definovat sadu zákazníků, kteří by měli být zpracováni ve snímku sledování splatnosti. Pokud v tomto poli vyberete fond zákazníků, je snímek sledování splatnosti vytvořen pouze pro účty odběratelů, které jsou součástí tohoto fondu zákazníků. Vybraný fond zákazníků musí být typu **Snímek sledování splatnosti**. Necháte-li toto pole prázdné, vytvoří se pro všechny účty zákazníků snímek sledování splatnosti.


- **Kritéria** - Snímek sledování splatnosti na základě data, které vyberete:

    - **Datum transakce** – Splatnost každé transakce bude splatná v závislosti na datu transakce.
    - **Datum splatnosti** – Splatnost každé transakce bude založena na datu splatnosti.
    - **Datum dokumentu** – Splatnost každé transakce bude založena na datu dokumentu.

- **Sledování splatnosti k** – Vyberte datum, které chcete použit jako **aktuální datum** pro snímek sledování splatnosti. Období pro sledování splatnosti se počítá na základě tohoto data. 

    - **Aktuální datum** – Použije se systémové datum. Tuto možnost vyberte, pokud je zpracování nastaveno v opakujících se dávkách. Poté se při každém spuštění dávky použije systémové datum daného spuštění.
    - **Vybrané datum** – Použije se vámi zadané datum. Pokud vyberete tuto možnost, musíte také zadat datum sledování splatnosti.

   Například aktuální období pro sledování splatnosti je 30 dní. Pokud v tomto poli vyberete **Dnešní datum**, aktuální období pro sledování splatnosti začíná dnešním dnem a poté zahrnuje předchozích 29 dní. Pokud v tomto poli vyberete **Vybrané datum** a zadáte datum, aktuální období pro sledování splatnosti začíná zadaným datem a poté zahrnuje předchozích 29 dní.

- **Aktualizovat stav kolekce** - Nastavte tuto možnost na **Ano**, abyste mohli aktualizovat stav shromažďování transakcí na stránce **Kolekce** ze stránky **Slib zaplacení** na **Slib zaplacení porušen**, pokud je datum sledování splatnosti po datu poli **Datum slibu zaplacení**. Tuto možnost nastavte na **Ne**, aby byl stav kolekce na stránce **Kolekce** beze změny.
- **Zahrnout zákazníky s nulovým zůstatkem** - Nastavte tuto možnost na **Ano**, pokud chcete zahrnout všechny zákazníky bez ohledu na jejich zůstatek. Pokud zahrnete všechny zákazníky, doporučujeme vám zapnout obě funkce: **Vylepšení výkonu sledování splatnosti zákazníka** a **Zlepšení výkonu sledování splatnosti zákazníka pomocí fondů zákazníků**. Tuto možnost nastavte na **Ne**, pokud chcete zahrnout pouze zákazníky, kteří mají zůstatek. Toto nastavení pomáhá urychlit výkon, protože zákazníci, kteří nemají zůstatek, jsou přeskočeni.
- **Obejít výpočty úvěrového limitu během sledování splatnosti** - Pokud je tato možnost nastavena na **Ano**, proces sledování platnosti nebude přepočítávat **Částku mezisoučtu na dodací listu**, **Částku mezisoučtu otevřené objednávky** a **Kredit k dispozici** pro každého zákazníka. Tyto zůstatky jsou uvedeny na stránce **Splatné zůstatky** v oknu s fakty v části **Úvěrový limit**. Chcete-li vyšší výkon během procesu sledování splatnosti, nastavte tuto možnost na **Ano**. Nastavte ji na **Ne**, chcete-li přepočítat zůstatky při spuštění procesu sledování splatnosti. 
- **Rozsah společnosti** - Na kartě **Rozsah společnosti** vyberte právnické osoby (společnosti), které chcete zahrnout do snímku sledování splatnosti. K výběru jsou k dispozici pouze právnické osoby, které jsou nastaveny pro centralizované platby. Transakce od vybraných právnických osob jsou poté zahrnuty do časových období u zákazníků, kteří mají ve všech těchto právnických osobách stejné ID strany. Částky v měně jsou převedeny na měnu právnické osoby, ke které jste přihlášeni při vytvoření snímku pro sledování splatnosti.

Doporučujeme naplánovat spuštění tohoto procesu v dávce.

> [!NOTE]
> Chcete-li pomoci zlepšit dávkový výkon při vytváření snímků sledování splatnosti, zadejte číslo do pole **Maximální počet dávkových úloh** na pevné záložce **Výchozí kolekce** na kartě **Kolekce** stránky **Parametry pohledávek**. V poli **Splatné zůstatky odběratelů** doporučujeme začít s hodnotou v intervalu **12** až **20** a poté hodnotu upravit tak, aby optimalizovala zpracování pro vaši situaci. Nedoporučujeme nastavovat tuto hodnotu na číslo větší než **30** protože to ovlivní výkon. 

