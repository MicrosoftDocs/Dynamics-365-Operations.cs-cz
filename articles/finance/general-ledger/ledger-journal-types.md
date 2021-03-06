---
title: Typy deníku hlavní knihy
description: Toto téma popisuje typy deníků, které lze nastavit pro finanční deníky.
author: ShylaThompson
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup
audience: Application User
ms.reviewer: roschlom
ms.custom: 15631
ms.assetid: 81613b31-bc3c-43a0-8474-e01c9a482c40
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34390014e0094518df45b1cc38e40ca4aa82de54
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823685"
---
# <a name="ledger-journal-types"></a>Typy deníku hlavní knihy

[!include [banner](../includes/banner.md)]

Toto téma popisuje typy deníků, které lze nastavit pro finanční deníky. Stránku **Názvy deníků** lze použít k nastavení deníků, které můžete používat v aplikaci Dynamics 365 Finance.

| Typ deníku                      | Účel                       | Zadejte transakce na této stránce                                |
|-----------------------------------|-------------------------------|----------------------------------------------------------------|
| Přidělení                        | Vytvořte transakce přidělení v deníku přidělení. Předtím, než budete moci vytvořit deník přidělení, je nejprve nutné vytvořit pravidlo přidělení na stránce **Hlavní kniha – pravidlo přidělení**.      | Požadavek na přidělení procesu             |
| Schválení                          | Zaúčtujte faktury dodavatele, které byly schváleny, do příslušných účtů hlavní knihy.  | Deník schválených faktur                                       |
| Storno bankovního šeku               | Stornujte zaúčtovaný šek. Chcete-li použít tento typ deníku, vyberte možnost **Použít proces kontroly pro storna plateb** na stránce **Parametry řízení hotovosti a banky**.   | Stornování šeků, storna plateb                   |
| Zrušení bankovní vkladové složenky    | Zrušte vkladovou složenku. Chcete-li použít tento typ deníku, vyberte možnost **Použít proces kontroly pro zrušení plateb vkladové složenky** na stránce **Parametry řízení hotovosti a banky**.   | Zrušení plateb vkladové složenky            |
| Rozpočet                            | Zpracujte přidělení rozpočtu. Chcete-li použít tento typ deníku, zaškrtněte možnost **Povolit rozdělení rozpočtu** na stránce **Parametry hlavní knihy**. Položky deníku rozpočtu budou obsahovat informace, které vychází z účtů hlavní knihy, které jsou definovány na stránce **Definice účtování**.                                                        |                                                                |
| Příjem cizí směnky odběratelem  | Vytvořte transakce přijetí odběratelů pro cizích směnky.             | Deník vystavení cizí směnky, Deník vystavených návratných cizích směnek |
| Bankovní převod odběratele          | Vytvořte soubory úhrady cizí směnky, který lze odeslat bance vaší společnosti. Chcete-li použít tento typ deníku, zrušte možnost **Automatické vyrovnání** na stránce **Parametry** **pohledávek**.            | Úhrada                                                     |
| Vystavení cizí směnky odběratelem    | Vytvořte transakce vystavení cizí směnky odběratelem. Chcete-li použít tento typ deníku, zrušte zaškrtnutí možnosti **Při zaúčtování faktur automaticky vytvořte a zaúčtujte deník vystavení** na stránce **Způsob platby – odběratelé**.   | Deník vystavení cizí směnky                                  |
| Platba odběratele                  | Vytvořte transakce plateb odběratelů.                             | Deník plateb             |
| Odběratel – protestovat cizí směnku | Vytvořte transakce protestování cizí směnky odběrateli.                    | Deník směnečného protestu                               |
| Odběratel – vystavit cizí návratnou směnku  | Vytvořte transakce započtení cizí směnky odběratelem.                     | Deník vystavených návratných cizích směnek                                |
| Odběratel – vyrovnat cizí směnku  | Vytvořte transakce vyrovnání cizí směnky odběrateli.                       | Deník vyrovnání cizí směnky                                |
| Denně                             | Vytvořte denní transakce v hlavním deníku.                          | Hlavní deník                                                |
| Eliminace                       | Vytvořte transakce eliminace v deníku eliminace. Chcete-li použít tento typ deníku, zaškrtněte možnosti **Použít pro proces finanční eliminace** a **Použít pro proces finanční konsolidace** na stránce **Právnické osoby**. Než budete moci použít tento typ deníku, je nutné vytvořit pravidlo eliminace hlavní knihy na stránce **Pravidlo eliminace hlavní knihy**. | Eliminace                                                    |
| Rozpočet dlouhodobého majetku                | Vytvořte položky registru rozpočtu dlouhodobého majetku.                                                                                                                                                                                                                                                                                                                 | Rozpočet dlouhodobého majetku                                             |
| Registr faktur                  | Zaregistrujte základní informace o fakturách dodavatele.                                                                                                                                                                                                                                                                                                           | Registr faktur                                               |
| Vyplacení mezd              | Vydejte platby podle mzdových výkazů. V tomto deníku nelze ručně zadat transakce. Je nutné generovat mzdové výkazy a poté je odeslat k platbě.                                                                                                                                                              |                                                                |
| Periodické                          | Vytvořte periodické transakce pro pravidelný deník.                                                                                                                                                                                                                                                                                                      | Periodické deníky                                              |
| Zaúčtovat dlouhodobý majetek                 | Zaúčtujte transakce dlouhodobého majetku.                                                                                                                                                                                                                                                                                                                              | Dlouhodobý majetek                                                   |
| Projekt – výdaje                | Vytvořte výdajové transakce projektu.                                                                                                                                                                                                                                                                                                                        | Expense                                                        |
| Úprava měny vykazování     | Vytvořte úpravy v měně vykazování pro zůstatky účtů hlavní knihy.               | Deníky úprav měny vykazování                         |
| Statistické transakce            | Vytvořte statistické transakce.                                                                                                                                                                                                                                                                                                                            |                                                                |
| Bankovní převod dodavatele            | Vytvořte soubor úhrady vlastní směnky, který lze odeslat bance vaší společnosti.                                                                                                                                                                                                                                                                      | Deník úhrad                                             |
| Úhrady dodavateli               | Vytvořte transakce úhrad dodavateli.                                                                                                                                                                                                                                                                                                                    | Deník plateb                                                |
| Vystavení vlastní směnky dodavateli       | Vystavte způsob platby prostřednictvím vlastních směnek dodavatele. Chcete-li použít tento typ deníku, zrušte zaškrtnutí možnosti **Při zaúčtování faktur automaticky vytvořte a zaúčtujte deník vystavení** na stránce **Způsob platby – dodavatelé**.                                                                                                                                          | Deník vlastních vystavených směnek                                   |
| Evidence faktur dodavatele – vyloučené zaúčtování | Vytvořte transakce faktury dodavatele, které nebyly dosud zaúčtovány do dočasného účtu doručení.                                                                                                                                                                                                                                                             | Podrobnosti evidence faktur dodavatelů bez zaúčtování                  |
| Evidence faktur dodavatele               | Vytvořte transakce evidence faktur dodavatele.                                                                                                                                                                                                                                                                                                                    |                                                                |
| Zápis faktury dodavatele          | Zaúčtujte faktury dodavatele, které jsou v deníku.                                                                                                                                                                                                                                                                                                                 | Deník faktur                                                |
| Dodavatel – vystavit návratnou vlastní směnku     | Znovu vystavte vlastní směnku, která již byla proplacena bankou vaší organizace.                                                                                                                                                                                                                                                                      | Deník vystavených návratných vlastních směnek                                 |
| Vyrovnání vlastní směnky dodavateli     | Vytvořte transakce vyrovnání vlastní směnky dodavateli.                                                                                                                                                                                                                                                                                                          | Deník vyrovnání vlastní směnky                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]