---
title: Nastavení šablony práce pro nákupní objednávky
description: Tento článek popisuje nastavení jednoduché pracovní šablony pro použití při odložení doručených položek.
author: Mirzaab
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee6bc896a979c326001e1596e4a463753005fabf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877356"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Nastavení šablony práce pro nákupní objednávky

[!include [banner](../../includes/banner.md)]

Tento článek popisuje nastavení jednoduché pracovní šablony pro použití při odložení doručených položek. Šablony práce určují sadu pokynů představovanou pracovníkovi skladu na mobilním zařízení, zatímco jsou položky přesouvány z místa příjmu. Můžete použít tuto proceduru s daty zmíněnými v ukázkových datech společnosti USMF. Před spuštěním tohoto průvodce vytvořte ID fondu práce. V tomto příkladu se používá ID fondu práce nazvaný Příchozí. Tento postup je určen pro vedoucího skladu.

1. V navigačním podokně přejděte na **Moduly > Řízení skladu > Nastavení > Práce > Pracovní šablony**.
2. V poli **Typ pořadí pracovních činností** vyberte možnost **Nákupní objednávky**.

## <a name="create-a-work-template-header"></a>Nadpis vytvoření šablony práce
1. Zvolte **Nové**.
2. V poli **Pořadové číslo** zadejte číslo. Toto je pořadí, ve kterém jsou vyhodnoceny šablony práce. Pořadí můžete v případě potřeby změnit.  
3. Zadejte hodnotu do pole **Šablona práce**. Toto je jedinečný identifikátor pro tuto šablonu.  
4. Zadejte hodnotu do pole **Popis pracovní šablony**.
    - Možnost **Platná** nebude zaškrtnuta, dokud nedoplníte veškeré informace, které jsou nutné pro šablonu, a pak jste vybrali **Uložit**.  
    - Pořadí pracovních činností typu **Nákupní objednávka** nelze zpracovat automaticky, proto ponechte možnost **Automatické zpracování** nastavenou na hodnotu **Ne**.  
5. Zadejte hodnotu do pole **ID pracovního fondu**. S ID fondů práce můžete uspořádat práci do skupin. Hodnota nastavená v tomto poli se bude výchozí hodnotou pro všechnu práci vytvořenou pomocí této šablony.  
6. Do pole **Priorita práce** zadejte číslo `1`. To ukazuje na význam práce a hodnoty, které nastavíte v tomto poli budou výchozí pro všechnu práci vytvořenou pomocí této šablony.  
7. Zvolte **Uložit**. Předtím, než bude k dispozici tlačítko **Upravit dotaz**, musíte uložit záhlaví šablony práce.  

## <a name="set-up-the-query-for-the-work-template"></a>Nastavit dotaz pro šablonu práce
1. Vyberte **Upravit dotaz**. Nastavíme omezení, že šablony lze použít jen v určitém skladu.  
2. Vyberte **přidat**.
3. Do pole **Pole** na novém řádku napište `warehouse`.
4. Zadejte hodnotu do pole **Kritéria**.
5. Vyberte **OK**.
6. Vyberte **Ano**.

## <a name="set-work-template-details"></a>Nastavit podrobnosti šablony práce
1. Zvolte **Nové**.
2. V poli **Typ práce** vyberte **Vybrat**.
3. Zadejte `purchase` do pole **ID pracovní třídy**. Pracovní třída, kterou nastavíte zde, bude výchozí pro všechny řádky práce typu Výdej, vytvořené pomocí této šablony. Třída práce nemůže být přepsána z řádků pořadí pracovních činností. Pracovní třídy se používají k nasměrování a/nebo omezení typu řádků pracovních objednávek, které pracovník skladu dokáže v mobilním zařízení zpracovat.  
4. Zvolte **Nové**.
5. V poli **Typ práce** vyberte **Vložit**.
6. Do pole **ID pracovní třídy** zadejte hodnotu. Jsou nastaveny pokyny pro výdej a příjem. Každá sada výdej/příjmu musí mít stejnou pracovní třídu. Používejte stejnou pracovní třídu, kterou jste zadali pro instrukci výdeje.  
7. Zvolte **Uložit**. Všimněte si, že je nyní zaškrtnuto zaškrtávací políčko **Platné**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]