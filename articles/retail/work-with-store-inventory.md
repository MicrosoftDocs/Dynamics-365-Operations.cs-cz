---
title: "Správa zásob na obchodě"
description: "Tento článek popisuje typy dokumentů, které můžete použít ke správě zásob."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 42091a5ec94bae3015fd9afca3ddcf1ef24f6eb4
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="manage-store-inventory"></a>Správa zásob na obchodě

[!include[banner](includes/banner.md)]


Tento článek popisuje typy dokumentů, které můžete použít ke správě zásob.

Typy následující dokumentů slouží ke správě skladových zásob v organizaci.

## <a name="purchase-orders"></a>Nákupní objednávky
Nákupní objednávky se vytvářejí v ústředí. Pokud je maloobchodní sklad zahrnut v záhlaví nákupní objednávky, objednávku lze přijmout v obchodě pomocí řešení Modern POS (MPOS) nebo Cloud POS v aplikaci Microsoft Dynamics 365 for Retail. Po zadání množství, která jsou přijata v obchodě, mohou být tato množství místně uložena pro další úpravy. Množství lze také potvrdit a odeslat do ústředí. V ústředí se množství, které bylo přijato v obchodě, zobrazuje v aplikaci Microsoft Dynamics 365 for Retail, v poli **Přijmout nyní** v nákupní objednávce.

## <a name="transfer-orders"></a>Převodní příkazy
Převodní příkaz může stanovit, že určitý obchod je místo, ze kterého mohou být položky expedovány. V tomto případě se převodní příkaz zobrazí v obchodě jako požadavek vyskladnění v MPOS nebo Cloud POS. Jakmile jsou požadovaná množství vyskladněna, jsou potvrzena a odeslána do ústředí. V ústředí se množství, které bylo vyzvednuto v obchodě, zobrazuje v aplikaci Microsoft Dynamics 365 for Retail v poli **Expedovat nyní** v převodním příkazu. Převodní příkaz může stanovit, že určitý obchod je místo, do kterého mohou být položky expedovány. V tomto případě se převodní příkaz zobrazí v obchodě jako příjmová žádanka v MPOS nebo Cloud POS. Po zadání množství, která jsou přijata v obchodě, mohou být tato množství místně uložena pro další úpravy. Množství lze také potvrdit a odeslat do ústředí. V ústředí se množství, které bylo přijato v obchodě, zobrazuje v aplikaci Microsoft Dynamics 365 for Retail, v poli **Přijmout nyní** v převodní objednávce.

## <a name="stock-counts"></a>Počty na skladě
Inventury mohou být plánované nebo neplánované. Plánované inventury zahajuje ústředí, které také určuje, které položky musí být spočítány. Ústředí vytvoří dokument inventury skladu, který lze přijmout v obchodě, kde jsou množství skutečných zásob na skladě zadána v MPOS nebo Cloud POS. Neplánované maloobchodní inventury jsou zahájeny v obchodě a množství skutečných zásob na skladě jsou aktualizována v MPOS nebo Cloud POS. Na rozdíl od plánovaných maloobchodních inventur nemají neplánované maloobchodní inventury předdefinovaný seznam položek. Po dokončení obou typů inventury budou potvrzeny a odeslány do ústředí. V ústředí bude inventura ověřena a zaúčtována.

## <a name="inventory-lookup"></a>Vyhledávání zásob
Na stránce vyhledávání zásob lze zobrazit aktuální množství produktu na skladě pro více obchodů a skladů. Kromě aktuálního množství na skladě je možné zobrazit budoucí množství, které lze slíbit (ATP) pro každý jednotlivý obchod. Chcete-li tak učinit, vyberte obchod, pro který chcete zobrazit ATP, a klikněte na **Zobrazit dostupnost obchodu**.




