---
title: "Integrace pro servisní smlouvy a projekty"
description: "Při práci se servisními smlouvami a řádky servisních smluv používáte data, která byla nastavená v oblastech řízení a účtování projektu."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9f2640eae299411d633c68795bc16883dbb5eeaf
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="integration-for-service-agreements-and-projects"></a>Integrace pro servisní smlouvy a projekty 

[!include [banner](../includes/banner.md)]


Při práci se servisními smlouvami a řádky servisních smluv používáte data, která byla nastavená v následujících oblastech **řízení a účtování projektu**.

## <a name="project-prices"></a>Projektové ceny

Náklady a prodejní cena transakce servisní smlouvy jsou odvozeny z nastavení nákladové ceny použité pro projekt, který je připojený k servisní smlouvě. Náklady a prodejní ceny lze nastavit podle projektu, zaměstnance a kategorie. 

## <a name="project-validation"></a>Ověření projektu

Projekty, zaměstnanci a kategorie, ze kterých lze vybírat na řádku servisní smlouvy, mohou být omezeny nastavením ověření v části **Řízení a účtování projektu**. Pomocí nastavení ověřování zaměstnanců, projektů a kategorií v nastavení ověření můžete řídit přístup. 

## <a name="project-line-properties"></a>Vlastnosti řádku projektu

Pro řádek servisní smlouvy se vlastnost řádku zadává automaticky.

Vlastnosti řádku se vytvářejí ve formuláři **vlastnosti řádku** v **řízení a účetnictví projektu**. Vlastnost řádku, která je zadána v servisní smlouvě, je připojena k projektu, který je vybrán pro servisní smlouvu a poté dědí řádek servisní smlouvy. 

## <a name="default-offset-accounts"></a>Výchozí protiúčty

Zadáte-li transakci nákladů, vybere se pro tuto transakci automaticky výchozí nákladový účet. Tento výchozí nákladový účet se nastavuje u projektu, který je připojený k aktuální servisní smlouvě.

## <a name="project-categories"></a>Kategorie projektů

Kategorie, které jsou dostupné pro řádky servisní smlouvy, se nastavují ve formuláři **Kategorie projektu** v části **Řízení a účtování projektu**. 

> [!NOTE]
> <P>Lze vybrat kategorie, které mají zaškrtnuté políčko <STRONG>Aktivní v denících</STRONG> na kartě <STRONG>Projekt</STRONG> ve formuláři <STRONG>Kategorie projektu</STRONG>. Pokud je však zaškrtnuté políčko <STRONG>Neaktivní kategorie</STRONG> na kartě <STRONG>Deníky</STRONG> ve formuláři <STRONG>Parametry řízení projektu a účetnictví</STRONG>, lze vybrat všechny kategorie.</P>

## <a name="project-parameters"></a>Parametry projektu

Pokud je zaškrtnuté políčko **Propuštění pracovníci** na kartě **Deníky** v okně **Parametry řízení a účetnictví projektu**, můžete vybrat neaktivní zaměstnance a aktivní zaměstnance ve formulářích **servisní smlouvy** a **servisní zakázky**.

Dále můžete zpřístupnit pole **Počáteční čas** a **Koncový čas** na kartě **Projekt** ve formuláři **Servisní zakázky** a umožnit tak zadávání času zahájení a ukončení v řádcích servisní zakázky.

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>Povolení zadávání času zahájení a ukončení v servisních zakázkách

1.  Klikněte na **Řízení a účetnictví projektů** \> **Nastavení** \> **Parametry modulu Řízení a účetnictví projektu**.

2.  Klepněte na tlačítko **deníky** a zaškrtněte políčko **zobrazit časy zahájení a ukončení**.

3.  Klikněte na uzel **Řízení a účtování projektů** \> **Nastavení** \> **Deníky** \> **Názvy deníku**.

4.  Vyberte název deníku připojeného k servisní zakázce.

5.  Klepněte na kartu **Obecné** a zaškrtněte políčko **zobrazit časy zahájení a ukončení**.


> [!NOTE]
> <P>Vyberte název deníku pro servisní zakázku v poli <STRONG>Hodina</STRONG> na kartě <STRONG>Deníky</STRONG> ve formuláři <STRONG>Parametry správy služby</STRONG>.</P>





