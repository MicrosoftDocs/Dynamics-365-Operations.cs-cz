---
title: "Měrná jednotka a zásady uskladnění"
description: "Tento článek popisuje způsob, jakým jsou výchozí jednotky, řady jednotek a převody jednotek používány v procesech skladu."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e0a22e07f5a0e5bc30c8ad9dc87c5a506d62847d
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# Měrná jednotka a zásady uskladnění

[!include[banner](../includes/banner.md)]


Tento článek popisuje způsob, jakým jsou výchozí jednotky, řady jednotek a převody jednotek používány v procesech skladu.

Skupiny klasifikace jednotky definují pořadí jednotek, které lze použít v operacích skladu. Jsou vytvořeny na stránce **Skupiny klasifikace jednotek**. Klasifikace ukazuje vztah různých jednotek. Například skladujete palety, které obsahují krabice, které obsahují jednotlivé položky. V takovém případě je třeba zadat tři různé jednotky a logické pořadí vrstev. Skupiny klasifikace jednotek umožňují definovat zásady pro seskupení registračních značek a výchozích jednotek, které chcete použít pro různé procesy skladu. Tento článek se vztahuje na rozšířené skladové řešení, které je k dispozici v modulu Řízení skladu, ale i jednodušší skladová řešení, která jsou k dispozici v modulu Řízení zásob.

## Skupiny klasifikace jednotek pro uvolněné produkty
Pokud chcete použít uvolněné produkty v pracovních procesech skladu, skupina klasifikace jednotek musí být k nim přiřazena. Pokud ověřujete produkt, který je přidružen ke skupině dimenzí úložiště a možnost **Používat procesy správy skladu** pro skupinu dimenzí úložiště je nastavena na **Ano**, zobrazí se chybová zpráva, pokud není ID skupiny klasifikace jednotek definováno pro produkt. Pokud skupina klasifikace jednotek, kterou používáte, obsahuje více řádků (a tedy více jednotek), musíte nastavit převod jednotek mezi jednotkami. K dokončení tohoto nastavení použijte stránku **Převody jednotek**. Nejmenší jednotkou v rámci skupiny klasifikace, kterou přidružíte k vydanému produktu, se musí shodovat se skladovou jednotkou, která je definována pro odpovídající produkt. Skladová jednotka je jednotka, která je použita pro základní výpočty množství na skladě. Převody měrné jednotky pro varianty produktu u základních produktů lze nastavit také pomocí možnosti **Povolit převody měrné jednotky**.

## Seskupení registračních značek
Můžete upřesnit, zda příjmy menší než nebo větší než jedna zadaná jednotka by měly být seskupeny do jedné registrační značky nebo rozděleny do více registračních značek pro každou jednotku. K nastavení tohoto chování použijte možnost **Seskupení poznávacích značek** na kartě **Podrobnosti řádku** na stránce **Skupiny klasifikace jednotek**. Pokud chcete použít seskupení registračních značek při zpracování práce pomocí mobilního zařízení, musíte vybrat možnost **Seskupení registračních značek** na položce nabídky **Mobilní zařízení**. Například pomocí mobilního zařízení můžete zaregistrovat položku, která je přidružená ke skupině klasifikace jednotek, která obsahuje dva řádky. První řádek je pro Kusy a možnost **Seskupení poznávacích značek** je nastavena na **Ano**. Druhý řádek je pro Jednotka palety a možnost **Seskupení poznávacích značek** je nastavena na **Ne**. V takovém případě systém může automaticky určovat, jak rozdělit a vytvořit registrační značky pro 100 kusů.

## Jednotky pro cyklickou inventuru
Pro definování jednotek, které chcete použít v rámci procesu cyklické inventury, vyberte možnost **Použít jednotku pro cyklickou inventuru** na stránce **Skupiny klasifikace jednotek**. Můžete vybrat maximálně čtyři jednotky do skupiny klasifikace. Pokud jste vybrali více než čtyři jednotky, další jednotky nebudou zobrazeny v mobilním zařízení.

## Výchozí jednotky pro procesy příjmu na mobilní zařízení
Pro nastavení výchozích jednotek, které chcete použít pro procesy příjmu u mobilního zařízení, povolte možnost **Výchozí jednotka pro nákup a převod** a **Výchozí jednotka pro výrobu** na stránce **Skupiny klasifikace jednotek**. Například lze určit, že standardně systém má při obdržení nákupní objednávky na skladě pomocí mobilního zařízení použít množství palet, ale skladová jednotka musí být Kusy. Chcete-li získat převodu pro počet kusů, které obsahuje každá paleta, je nutné definovat převodní jednotky, jako je 100 kusů = 1 paleta.

## Výchozí nastavení objednávky
Při vytvoření uvolněných produktů je nutné vybrat výchozí jednotky pro nákup, prodej a sklad a zpracovat tak různé objednávky. Můžete nastavit výchozí jednotky a množství pro různé zdrojové dokumenty pomocí stránek **Výchozí nastavení objednávky** a **Nastavení objednávky specifické pro pracoviště**. Tyto stránky lze otevřít pomocí stránky **Uvolněné produkty**.




