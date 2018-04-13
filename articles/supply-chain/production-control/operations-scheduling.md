---
title: "Plánování operací"
description: "Toto téma obsahuje obecné informace o plánování operací. Plánování operací můžete použít, když je třeba získat obecný odhad výrobního procesu v čase."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 198073
ms.assetid: 12c28b11-80aa-4668-b15b-724cb24890bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 81dec9d988b22959df5421b7b84ef532a28e1228
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="operations-scheduling"></a>Plánování operací

[!INCLUDE [banner](../includes/banner.md)]

Toto téma obsahuje obecné informace o plánování operací. Plánování operací můžete použít, když je třeba získat obecný odhad výrobního procesu v čase.

Můžete naplánovat výrobu na úrovni operací a pracovního zařazení. Na rozdíl od plánování práce se plánování operací nerozšiřuje na operace pro výrobní postup úloh. Pokud chcete zahrnout podrobnější informace o plánování, například informace o aktuální kapacitě, můžete spustit plánování úloh po provedení plánování operací. Můžete spustit také pouze plánování úlohy. Plánování práce se obvykle používá k plánováním jednotlivých úloh v dílně a obvykle je prováděno v krátkodobém až střednědobém časovém horizontu.

## <a name="components-of-operations-scheduling"></a>Komponenty plánování operací
Hlavními komponentami plánování operací jsou směr plánování, kapacita prostředků a optimalizace materiálu. Pomocí plánování operací můžete dosáhnout těchto cílů:

-   Řízení metody plánování dopředným nebo zpětným plánováním od daného data.
-   Optimalizace využití zdrojů naplánováním výroby na základě kapacity zdrojů. Tento přístup také pomáhá určit, kdy mají být použity alternativní zdroje.
-   Optimalizace využití materiálů naplánováním výroby na základě dostupnosti požadovaných materiálů.
-   Naplánujte a synchronizujte referenční výroby? Když se změní plán výrobní zakázky, jsou upravena data referenční výroby.

Musíte odhadnout náklady na výrobní zakázku a teprve potom začít s plánováním operací. Pokud jste odhad neprovedli, automaticky se spustí před zahájením plánování operací. Plán operací určuje následující informace:

-   Produkt plánovaný pro výrobu
-   Konfigurace produktu
-   Množství, která jsou součástí výroby
-   Data zahájení a ukončení výroby
-   Rezervace kapacity zdrojů provádějících výrobní činnosti

Čas nastavení, doba zpracování a čas zpracování jsou nastaveny pro operace ve výrobě. Po provedení plánování operací je stav výrobní zakázky **Plánováno** a jsou naplánována za všechny operace v pořadí, které je určeno ve výrobním postupu. Bere se však v úvahu pouze doba trvání operace. Počáteční a koncový čas se neplánují.

## <a name="scheduling-direction-and-date"></a>Způsob a datum plánování
Způsob plánování je základním faktorem procesu plánování. Výrobu lze naplánovat dopředu nebo zpětně od libovolného data v závislosti na požadavcích načasování a plánování.

-   **Dopředu od data plánování** – výrobu můžete naplánovat tak, aby se zahájila co nejdříve. Může začít dnes, zítra nebo ke kterémukoli určenému budoucímu datu. Výroba je naplánována předem k nejbližšímu možnému koncovému datu.
-   **Zpět od data plánování** – výrobu můžete naplánovat tak, aby se zahájila co nejpozději. Zpětné plánování je založeno na datu, kdy musí být výroba dokončena. Plán se počítá zpětně od tohoto data do nejpozdějšího možného data, kdy může výroba může začít a být dokončena včas.

## <a name="resource-scheduling"></a>Plánování prostředků
Při provádění plánu operací se každé z operací ve výrobním postupu naplánuje datum provedení prostředkem určeným pro danou operaci. Kromě toho je ve výrobním postupu uvedeno trvání jednotlivých operací. Pokud je pro operaci určena skupina prostředků, plánování rezervuje potřebnou kapacitu ve skupině. Avšak na rozdíl od plánování práce nevybírá plánování operací konkrétní prostředek ve skupině. Pokud pracujete s omezenou kapacitou, plán závisí na dostupnosti provozních prostředků, které jsou zapotřebí k dokončení výroby. Plánování operací postupuje po jednotlivých operacích specifikovaných ve výrobním postupu. Plánování operací rezervuje kapacitu skupin prostředků podle provozních dob definovaných ve výrobním postupu. Kapacitu skupiny prostředků určuje součet dostupné kapacity prostředků, které jsou zahrnuty. Rezervace kapacity, které již existují pro prostředky, jsou považovány za nedostupnou kapacitu. Není-li k dispozici dostatek kapacity pro výrobu, výrobní zakázky se mohou zpozdit nebo i zastavit. Můžete také určit účinnost, kterou očekáváte od prostředků, které jsou zahrnuty do výroby. Jako procentuální hodnotu prostředku zadáte efektivitu. Procento efektivity upraví propustnosti prostředku. Toto nastavení ovlivňuje dobu rezervovanou pro prostředek. Jsou také náležitě upraveny doby realizace pro operace, které používají prostředek.

## <a name="operations-scheduling-and-master-planning"></a>Plánování operací a hlavní plánování
Plán operací také řídí hlavní plánování a určuje výpočty požadavků na materiál. Plán operací zohledňuje následující informace:

-   **Nedokončená výroba** – plánované, uvolněné nebo zahájené produkty
-   **Dostupnost materiálu** – zásoby, dílčí výroba a dodavatelé
-   **Dostupnost kapacity** – zdroje, které jsou nutné pro výrobu

## <a name="cancellations"></a>Zrušení
Když spustíte plánování operací, můžete zrušit konkrétní částí postupu. Následující části obsahují dobu ve frontě, přípravný čas, dobu zpracování, čas překrytí a doby přepravy.

## <a name="finite-materials"></a>Omezený materiál
Pokud pracujete s hotovými materiály, plánování je závislé také na dostupnosti materiálů potřebných k výrobě. Pokud není k dispozici dostatek součástí pro výrobu, může být výroba zpožděna. Plánování můžete založit na použití materiálů zadáním materiálů, které musí být k dispozici pro výrobu. Při optimalizaci kapacity prostředků a dostupnosti materiálů je výroba vypočtena podle těchto omezení. Zahájení výrobní zakázky nelze naplánovat, dokud nebude k dispozici veškerá kapacita a materiály současně a v požadovaných množstvích.

<a name="see-also"></a>Viz také
--------

[Možnosti plánování operací](operation-scheduling-options.md)




