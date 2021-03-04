---
title: Rozvrhnout plány údržby
description: Toto téma popisuje rozvrhování plánů údržby v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: df5bcd57c611ed5f77a417a28f28fca84057d734
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423926"
---
# <a name="schedule-maintenance-plans"></a>Rozvrhnout plány údržby

[!include [banner](../../includes/banner.md)]

 

Preventivní plánování údržby vygeneruje položky kalendáře na majetku na základě plánů údržby nastavených na majetku. Můžete plánovat položky v kalendáři na základě vybraných plánů údržby, typů majetku a majetku.

1. Klikněte na **Správa majetku** > **Periodické** > **Preventivní údržba** > **Rozvrhnout plány údržby**.

2. V polích **Období** a **Frekvence** můžete vybrat časový interval.

>[!NOTE]
>Pole **Období** a **Frekvence období** určují, jak moc předem má být vytvořen řádek plánu údržby na základě plánů údržby, které jste vytvořili (založené na čase nebo na základě čítače). Na následujícím obrázku jsou řádky plánu údržby (= návrhy pracovních příkazů) vytvořeny od aktuálního data po dobu tří měsíců.

3. V případě, že se mají automaticky vytvářet pracovní příkazy podle řádku plánu údržby, vyberte možnost Ano na kartě **Automaticky vytvořit, pokud je to uvedeno v řádku**.

>[!NOTE]
>Je-li toto přepínací tlačítko nastaveno na hodnotu „Ano“ *a* políčko **Automaticky vytvořit** je také zaškrtnuto na řádcích plánu údržby v **Plánech údržby**, budou vytvořeny pracovní příkazy na základě řádků plánu údržby a budou vytvořeny také řádky plánu údržby se stavem „Pracovní příkaz vytvořen“. Je-li vybrána pouze jedna možnost (přepínač **Automaticky vytvořit, pokud je to uvedeno v řádku** v tomto dialogovém okně nebo zaškrtávací políčko **Automaticky vytvořit** ve formuláři **Plány údržby**), budou vytvořeny pouze řádky plánu údržby se stavem „Vytvořeno". V takovém případě se žádné pracovní příkazy nevytvoří.

4. Je možné generovat položky kalendáře na základě plánů údržby (čas nebo čítač), majetku, typů majetku, funkčních míst a typů funkčních umístění. Klepněte na tlačítko **Filtr** a proveďte výběr, pokud je to nutné.

- V souvislosti s rozvrhováním plánů údržby ve funkčních místech: Pokud aktualizujete nastavení typů majetku, výrobců a modelů v plánech údržby na pevné záložce **Všechna funkční umístění** > **Plány údržby** po provedení plánovaných plánů údržby, existující položky plánu údržby vztahující se k tomuto funkčnímu umístění jsou automaticky odstraněny. Chcete-li vytvořit nové položky kalendáře, které odpovídají nastavení aktualizovaného plánu údržby na funkčním místě, musíte pro toto funkční místo spustit nový plán plánu údržby. Další informace o nastavení typů majetku, výrobců a modelů ve funkčních umístěních naleznete v části [Vytváření funkčních míst](../functional-locations/create-functional-locations.md).

>*Příklad:* chcete vytvořit plán údržby pro konkrétní funkční místo, což znamená, že všechny majetky nastavené v tomto funkčním místě budou při plánování plánu údržby zahrnuty v daném čase. V takovém případě vytvořte plán údržby a vyberte konkrétní funkční místo, ale NEPŘIDÁVEJTE do plánu údržby žádná aktiva. Výsledkem je, že při rozvrhování plánu údržby budou pro všechny majetky související se funkčním místem v daném okamžiku vytvořeny řádky plánu údržby.

- Pokud provedete změny typů majetku, výrobců a modelů v **Typech majetku**, budou tyto změny mít vliv pouze na nový majetek, který používá aktualizovaný typ majetku. Další informace o nastavení typu majetku v [Typech majetku](../setup-for-objects/object-types.md)  

5. Kliknutím na tlačítko **OK** zahájíte generování položek plánu údržby na majetku. Vygenerované položky budou zobrazeny na stránce se seznamem **Všechny plány údržby**. Následující ilustrace znázorňuje příklad sestavy **Plány rozvrhu údržby**.

![Obrázek č. 1](media/09-preventive-maintenance.png)

- V dialogovém okně **Rozvrhnout plány údržby** můžete nastavit dávkové úlohy na pevné záložce **Spustit na pozadí** pro automatické generování položek kalendáře v pravidelných intervalech.  
- Při plánování preventivní údržby nebudou vytvořeny řádky plánu údržby s očekávaným počátečním datem a časem, které předchází systémovému datu a času.  

Následující obrázek poskytuje grafické znázornění výpočtu plánu údržby založené na čase.  

![Obrázek č. 2](media/10-preventive-maintenance.jpg)

V souvislosti s plány údržby založenými na čítačích: v následujících obrázcích jsou zobrazeny dva různé cykly registrace čítačů. Jsou založeny na plánu údržby nastaveném pro majetek "V0001", což předpokládá, že majetek (auto) najede přibližně 2 000 km každý měsíc.

V prvním příkladu očekávaných 2 000 km není dosaženo každý měsíc. Podle plánu údržby založeném na čítači je prahová hodnota 2 000 km, což znamená, že při spuštění plánování plánu údržby by měl být při každém dosažení prahové hodnoty 2 000 km vytvořen řádek plánu údržby. V příkladu 1 existují 4 řádky registrace, ale prahové hodnoty 2 000 km bylo dosaženo pouze jednou. To znamená, že když spustíte rozvržení plánu údržby, bude pro tento majetek, například v období 3 měsíců, vytvořen pouze jeden řádek plánu údržby.

Na dalším obrázku je každý měsíc registrováno 2 000 km nebo více. Pokud tedy naplánujete plány údržby pro tento majetek v období 3 měsíců, vytvoří se tři řádky údržby. 

Zde popsané příklady znázorňují, že všechny registrace čítačů provedené na majetku ukazují trend popisující opotřebení majetku. Tato funkce se používá jako základ výpočtu v době plánování plánu údržby.

![Obrázek č. 3](media/11-preventive-maintenance.png)

![Obrázek č. 4](media/12-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]