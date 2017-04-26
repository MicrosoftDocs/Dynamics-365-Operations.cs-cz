---
title: "Konfigurace vyrovnání"
description: "To, jak a kdy jsou transakce vyrovnány, může být poměrně složité, proto je nutné pochopit a správně definovat parametry pro splnění požadavků společnosti. Tento článek popisuje parametry, které se používají k vyrovnání pro závazky i pohledávky."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 6927ed98c82f174a18d3d8821fbdb302801835c4
ms.lasthandoff: 03/31/2017


---

# <a name="configure-settlement"></a>Konfigurace vyrovnání

[!include[banner](../includes/banner.md)]


To, jak a kdy jsou transakce vyrovnány, může být poměrně složité, proto je nutné pochopit a správně definovat parametry pro splnění požadavků společnosti. Tento článek popisuje parametry, které se používají k vyrovnání pro závazky i pohledávky. 

Tyto parametry ovlivňují zpracování vyrovnání v Microsoft Dynamics 365 pro operace. Vyrovnání je proces vyrovnání faktury podle platbou nebo dobropisem. Tyto parametry jsou umístěny v oblasti **Vyrovnání** stránek **Parametry pohledávek** a **Parametry závazků**.

-   **Automatické vyrovnání** – nastavte možnost na hodnotu **Ano**, má-li se transakce automaticky vyrovnat oproti otevřeným transakcím při zaúčtování. Je-li tato možnost je nastavena na hodnotu **Ne**, uživatelé mohou transakce vyrovnat ručně při zadávání plateb nebo později pomocí stránky **Vyrovnat transakce**.
-   **Správa hotovostní slevy** – zadat jak [platební sleva je zpracována, když je přeplatili fakturu](cash-discount-handling-overpayments.md). Přeplatek platební sleva může být snížena, lze považovat za rozdíl nebo mohou zůstat na účet dodavatele nebo zákazníka.
    -   **Neurčeno** – částka platební slevy se sníží o částku přeplatku. Toto chování se vždy používá bez ohledu na to, zda je částka přeplatku větší nebo menší než částka zadaná v poli **Maximální přeplatek či nedoplatek**.
    -   **Specifické** – částka přeplatku buď je zaúčtována na účet hlavní knihy s rozdílem platební slevy, nebo zůstane zůstatek na účtu odběratele nebo dodavatele. Specifické chování závisí na tom, zda je částka přeplatku mezi 0,00 a částkou zadanou v poli **Maximální přeplatek či nedoplatek**, nebo zda je částka přeplatku větší než částka **Maximální přeplatek či nedoplatek**.
-   **Maximální haléřový rozdíl** – zadejte maximální povolený haléřový rozdíl pro vyrovnané transakce. Je-li rozdíl menší nebo rovný haléřovému rozdílu určenému v tomto poli, rozdíl se zaúčtuje na účet haléřových rozdílů v hlavní knize uvedený na stránce **Účty pro automatické transakce**.
-   **Maximální přeplatek či nedoplatek** – zadejte částku, která se přijme jako přeplatek a nedoplatek. Chcete-li vypočítat daň u přeplatků či nedoplatků, na stránce **Parametry hlavní knihy** klikněte na volbu **DPH** a zvolte možnost **DPH při nedoplatku nebo přeplatku**.
    -   Pokud přeplatek či nedoplatek tvoří rozdíl menší než je rozdíl určený v poli **Maximální haléřový rozdíl**, částka haléřového rozdílu bude zaúčtována na účet haléřových rozdílů
    -   Pokud přeplatek či nedoplatek tvoří rozdíl větší než je rozdíl určený v poli **Maximální haléřový rozdíl**, částka rozdílu bude zaúčtována na účet rozdílů vybraný pro typ zaúčtování **Platební sleva odběratele** nebo **Platební sleva dodavatele** na stránce **Účty pro automatické transakce**.
-   **Vypočítat platební slevy pro částečné platby** – nastavte možnost na hodnotu **Ano**, chcete-li povolit, aby se platební slevy automaticky vypočítávaly pro částečné platby.
    -   Účinek této možnosti závisí na hodnotě v poli **Použít platební slevu** na stránce **Vyrovnat transakce**. Je-li tato možnost je nastavena na hodnotu **Ano**, sleva je přijata při nastavení pole **Použít platební slevy** na hodnotu **Normální**. Pokud je pole **Použít platební slevy** nastaveno na hodnotu **Vždy**, platební sleva je vždy přijata bez ohledu na nastavení v tomto poli. Pokud je pole **Použít platební slevu** nastaveno na hodnotu **Vždy**, platební sleva je vždy přijata bez ohledu na nastavení v tomto poli.
    -   Je-li tato možnost nastavena na hodnotu **Ano** a uživatel změní hodnot v poli **Částka k vyrovnání** na stránce **Vyrovnat transakce**, sleva se vypočítá automaticky a bude zobrazena jako výchozí hodnota v poli **Částka platební slevy k přijetí**.
    -   Je-li tato možnost nastavena na hodnotu **Ne** a uživatel provede změnu hodnoty v poli **Částka k vyrovnání** na stránce **Vyrovnat transakce**, jako výchozí hodnota v poli **Částka platební slevy k přijetí** se použije hodnota **0** (nula).
-   **Vypočítat platební slevy pro dobropisy** – nastavte možnost na hodnotu **Ano**, aby se automaticky vypočítala platební sleva pro dobropisy. V části Pohledávky je transakce dobropisu záporná transakce s hodnotou v poli **Faktura** na stránce **Volná faktura** nebo vrácení na stránce **Prodejní objednávka**.
    -   Účinek této možnosti závisí na hodnotě v poli **Použít platební slevu** na stránce **Vyrovnat transakce**. Pokud je tato možnost nastavena na **Ano**, sleva uplatněna při *** použití platební slevy *** je nastaveno na **normální**. Když *** použití platební slevy *** je nastaveno na **vždy**, platební sleva je vždy přijata bez ohledu na nastavení tohoto pole. Když *** použití platební slevy *** je nastaveno na **nikdy**, platební sleva nikdy není přijato, bez ohledu na nastavení tohoto pole.
    -   Je-li tato možnost nastavena na hodnotu **Ano** a dobropis je označený na stránce **Vyrovnat transakce**, sleva se vypočítá automaticky a bude zobrazena jako výchozí hodnota v poli **Částka platební slevy k přijetí**.
    -   Je-li tato možnost nastavena na hodnotu **Ne** a dobropis je označený na stránce **Vyrovnat transakce**, bude jako výchozí hodnota v poli **Částka platební slevy k přijetí** použita hodnota **0** (nula).
-   **Slevové protiúčty (pouze závazky)** – definujte výchozí účetní knihy platebních slev, která má být použita pro účetní položku pro platební slevy.
    -   **Použít hlavní účet slev pro dodavatele** – platební sleva je zaúčtována pro hlavní účet, který je definován na stránce **Nastavení platební slevy**.
    -   **Účty na řádcích faktury** – platební sleva je zaúčtována na účty hlavní knihy pro původní fakturu.
-   **Označit řádky na volných fakturách a oznámeních úroků (pouze pohledávky)** – nastavte možnost na hodnotu **Ano**, abyste aktivovali tlačítko **Označit řádky faktury** na stránkách **Zadat platby odběratele**, **Platební doklad deníku** a **Vyrovnat transakce**. Toto tlačítko umožňuje označit jednotlivé řádky pro vyrovnání.
-   **Určit prioritu vyrovnání (pouze pohledávky)** – nastavte možnost na hodnotu **Ano**, abyste aktivovali tlačítko **Označit podle priority** na stránkách **Zadat platby odběratele** a **Vyrovnat transakce**. Toto tlačítko umožňuje uživatelům přiřadit pořadí předem vyrovnání transakce.  Po pořadí vyrovnání byla vyrovnána transakce, pořadí a přidělení platby lze změnit před zaúčtováním.
-   **Použít prioritu pro automatické vyrovnání** – nastavte možnost **Ano** použití definovaných priorit při transakce budou automaticky vyrovnány. Toto pole je dostupné pouze tehdy, pokud **určit prioritu vyrovnání** a **automatické vyrovnání** možností **Ano**.





