---
title: "Přehled provizí v Retail POS pomocí prodejní skupiny"
description: "Je běžnou praxí maloobchodní prodej sledovat pomocí přidružení, které pracovaly se zákazníkem, poskytování pomoci, nabízení, prodejem a zpracování transakce."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dfefdede8f3bc884b230109d6c915127a1361ecd
ms.lasthandoff: 03/31/2017


---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Přehled provizí v Retail POS pomocí prodejní skupiny

[!include[banner](includes/banner.md)]


Je běžnou praxí maloobchodní prodej sledovat pomocí přidružení, které pracovaly se zákazníkem, poskytování pomoci, nabízení, prodejem a zpracování transakce.

Sledování prodeje prodejní zástupce je míra associates prodejní schopnosti, zatímco prodeje podle pokladníka je měření rychlosti a účinnosti. Sledovány obchodní zástupce prodeje se také často používají k výpočtu provize nebo jiné pobídky.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Konfigurace pracovník prodeje reprezentativní v Retail POS
Pracovník je přidán do prodejní skupiny, se stanou způsobilé pro Komisi a může být identifikován jako obchodní zástupce v systému. Pracovník, který není ve skupině prodejní není způsobilé pro Komisi a nebudou uvedeny jako obchodní zástupce do místa prodeje (POS) aplikace. V Retail POS seznam obchodních zástupců je odvozen ze všech prodejních skupin, které obsahují alespoň jeden pracovník přiřazen k úložišti. Seznam je uveden v POS jako kombinaci prodejní název a ID skupiny (ID: název). Výchozí prodejní skupiny lze přiřadit pracovníkům pro podporu scénářů, kde prodejce rozhodne nastavit prodejní zástupce na řádcích POS automaticky. Uživatelé mohou vybrat z prodejní skupiny, kterou pracovník je členem.

## <a name="functionality-profile-settings"></a>Nastavení funkce profilu
Existuje několik nastavení funkce profilu pro obchod, který určuje tok a proces v Retail POS, která zahrnuje obchodní zástupce.

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Profile**                           | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Default to cashier when available** | Pokud je tato možnost povolena, POS automatické vyplnění řádků transakcí s aktuální pokladník výchozí prodejní skupiny. Pokud pokladník nemá výchozí prodejní skupiny zadán, hodnota nebude nastavena. Uživatel může ručně nastavit prodejní skupiny pomocí mřížky tlačítko POS.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Prompt for sales representative**   | Tato možnost má tři možné hodnoty: ** Ne **-Pokud je vybrána tato možnost, uživatel nebude vyzván vyberte skupinu daně. Hodnota může být stále nastavena pomocí skupiny Prodej pokladník výchozí nebo ručně pomocí POS tlačítko mřížky. **Počáteční transakce** - Pokud je tato volba vybraná a buď **pokladník ve výchozím nastavení** není povolena možnost nebo aktuální pokladník nemá výchozí prodejní skupiny, uživatel bude vyzváni k výběru prodejní skupiny na začátku každé transakce. Výběrem prodejní skupiny z příkazového řádku, budou všechny následné řádky vybrané prodejní skupiny výchozí. Uživatel může ručně nastavit prodejní skupiny pomocí mřížky tlačítko POS. **Pro každý řádek** - Pokud je tato volba vybraná a buď **pokladník ve výchozím nastavení** není povolena možnost nebo aktuální pokladník nemá výchozí prodejní skupiny, uživatel bude vyzváni k výběru prodejní skupiny po přidání každého řádku. Uživatel ručně nastavit prodejní skupiny pomocí mřížky tlačítko POS. |
| **Vyžadují**                           | Tuto možnost lze použít, pouze pokud POS je nakonfigurován pro zadání obchodního zástupce. Je-li povoleno, uživatel bude muset před pokračováním vyberte skupinu daně. V opačném uživatel vyzváni, ale můžete zrušit a pokračovat bez provedení výběru. Po přidání řádku může uživatel s dostatečnými oprávněními stále odeberte z řádku prodejní skupiny. V této situaci není vynucena "Požadovat prodejní zástupce".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Zobrazení na obrazovce POS transakcí prodeje reprezentativní údaje
Rozvržení obrazovky POS transakcí a obsah jsou konfigurovatelné pomocí rozložení obrazovky rozvržení obrazovky návrháře a přiřazené obchody, registry nebo pracovníků. **Prodejního zástupce** lze přidat pole na kartě řádky v podokně účtenky.  Zobrazí se ID zadané skupiny prodeje pro každý řádek v okně transakce.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Přidání prodejní zástupce operace POS tlačítko mřížky
POS umožňuje uživatelům konfigurovat mřížek tlačítek, které jsou součástí rozložení obrazovky poskytují přístup k POS operací. Tlačítka mřížky tlačítek, které se týkají obchodního zástupce lze přiřadit následující operace POS.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Operace**                             | **Description**                                                                                                                                                                                                                                                                              |
| Nastavit prodejního zástupce na řádku          | Tato operace Retail POS zobrazí seznam způsobilých prodejní skupiny (ID: název) pro úložiště. Výběr ze seznamu prodejní skupiny nastavte hodnotu na aktuálním řádku transakce.                                                                                                            |
| Vymazat prodejního zástupce na řádku        | Tato operace POS odstraní aktuální hodnotu skupiny prodeje z aktuálního řádku transakce.                                                                                                                                                                                                  |
| Nastavit transakce prodejního zástupce   | Tato operace Retail POS zobrazí seznam způsobilých prodejní skupiny (ID: název) pro úložiště. Skupina prodeje výběru z tohoto seznamu nastavit výchozí hodnotu pro aktuální transakci. Bez prodejní skupiny přiřadit existující řádky budou sady, jakož i všechny později přidané řádky. |
| Vymazat prodejce na transakci | Tato operace POS odebere aktuální výchozí hodnota skupiny prodeje z aktuální transakce. To nemá vliv na všechny řádky, které již existují v transakci.                                                                                                                             |

## <a name="calculating-commissions"></a>Výpočet provize
Pro pracovníky v zadané skupiny prodeje vypočítána provize v okamžiku zaúčtování výkazu nebo zaúčtování prodejní objednávky. Částka provize závisí na podílu zaměstnance Komise, podle prodejní skupiny a nastavení výpočtu přidružené Komise pro odběratele a produkty na transakci.




