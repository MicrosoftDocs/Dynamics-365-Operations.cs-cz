--- 
title: "Nastavení šablony práce pro nákupní objednávky"
description: "Tento postup se zaměřuje na nastavení jednoduché pracovní šablony pro použití při odložení doručených položek."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: aa561d558827e78529ef797b6df6dd3c1dcce34d
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Nastavení šablony práce pro nákupní objednávky

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup se zaměřuje na nastavení jednoduché pracovní šablony pro použití při odložení doručených položek. Šablony práce určují sadu pokynů představovanou pracovníkovi skladu na mobilním zařízení, zatímco jsou položky přesouvány z místa příjmu. Můžete použít tuto proceduru s daty zmíněnými v ukázkových datech společnosti USMF. Před spuštěním tohoto průvodce vytvořte ID fondu práce. V tomto příkladu se používá ID fondu práce nazvaný Příchozí. Tento postup je určen pro vedoucího skladu.

1. Přejděte do nabídky Řízení skladu > Nastavení > Práce > Pracovní šablony.
2. V poli Typ pořadí pracovních činností vyberte možnost Nákupní objednávky.

## <a name="create-a-work-template-header"></a>Nadpis vytvoření šablony práce
1. Klikněte na položku Nová.
2. V poli Pořadové číslo zadejte číslo.
    * Toto je pořadí, ve kterém jsou vyhodnoceny šablony práce. Pořadí můžete v případě potřeby změnit.  
3. Zadejte hodnotu do pole Šablona práce.
    * Toto je jedinečný identifikátor pro tuto šablonu.  
4. Zadejte hodnotu do pole Popis pracovní šablony.
    * Možnost Platná možnost nebude zaškrtnuta, dokud nedoplníte veškeré informace, které jsou nutné pro šablonu, a pak jste klepnuli na možnost Uložit.  
    * Pořadí pracovních činností typu Nákupní objednávka nelze zpracovat automaticky, proto ponechte možnost automatického zpracování nastavenou na hodnotu Ne.  
5. Zadejte hodnotu do pole ID pracovního fondu.
    * S ID fondů práce můžete uspořádat práci do skupin. Hodnota nastavená v tomto poli se bude výchozí hodnotou pro všechnu práci vytvořenou pomocí této šablony.  
6. Do pole Priorita práce zadejte číslo „1“.
    * To ukazuje na význam práce a hodnoty, které nastavíte v tomto poli budou výchozí pro všechnu práci vytvořenou pomocí této šablony.  
7. Klikněte na položku Uložit.
    * Předtím, než bude k dispozici tlačítko Upravit dotaz, musíte uložit záhlaví šablony práce.  

## <a name="set-up-the-query-for-the-work-template"></a>Nastavit dotaz pro šablonu práce
1. Klikněte na možnost Upravit dotaz.
    * Nastavíme omezení, že šablony lze použít jen v určitém skladu.  
2. Klepněte na možnost Přidat.
3. Označte v seznamu vybraný řádek.
4. Do pole Pole zadejte „sklad“.
5. Zadejte hodnotu do pole Kritéria.
6. Klikněte na tlačítko OK.
7. Klepněte na tlačítko Ano.

## <a name="set-work-template-details"></a>Nastavit podrobnosti šablony práce
1. Klikněte na položku Nová.
2. V poli Typ práce vyberte „Vybrat“.
3. Zadejte „nákup“ do pole ID pracovní třídy.
    * Pracovní třída, kterou nastavíte zde, bude výchozí pro všechny řádky práce typu Výdej, vytvořené pomocí této šablony. Třída práce nemůže být přepsána z řádků pořadí pracovních činností. Pracovní třídy se používají k nasměrování a/nebo omezení typu řádků pracovních objednávek, které pracovník skladu dokáže v mobilním zařízení zpracovat.  
4. Klikněte na položku Nová.
5. V poli Typ práce vyberte „Vložit“.
6. Zadejte hodnotu do pole ID pracovní třídy.
    * Jsou nastaveny pokyny pro výdej a příjem. Každá sada výdej/příjmu musí mít stejnou pracovní třídu. Používejte stejnou pracovní třídu, kterou jste zadali pro instrukci výdeje.  
7. Klikněte na položku Uložit.
    * Všimněte si, že je nyní zaškrtnuto platné zaškrtávací políčko.  


