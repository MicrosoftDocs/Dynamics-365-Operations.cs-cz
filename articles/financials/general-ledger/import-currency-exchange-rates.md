---
title: "Importovat směnné kurzy měn"
description: "Jestliže právnická osoba obdržela faktury v cizí měně, je nutné převést cizí měny na místní měnu. To znamená, že jsou potřeba aktuální směnné kurzy pro různé měny. Toto téma obsahuje přehled požadovaných nastavení a zpracování pro import referenčních směnných kurzů publikovaných prostřednictvím Internetu poskytovateli směnných kurzů, jako je Evropská centrální banka a centrální banky Ruska."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c80f6eec7c4d5129337b6f7869fbd8a4cc978acd
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="import-currency-exchange-rates"></a>Importovat směnné kurzy měn

[!include[banner](../includes/banner.md)]


Jestliže právnická osoba obdržela faktury v cizí měně, je nutné převést cizí měny na místní měnu. To znamená, že jsou potřeba aktuální směnné kurzy pro různé měny. Toto téma obsahuje přehled požadovaných nastavení a zpracování pro import referenčních směnných kurzů publikovaných prostřednictvím Internetu poskytovateli směnných kurzů, jako je Evropská centrální banka a centrální banky Ruska.

V následujících částech je popsán celkový tok informací, které se používají k nastavení a zpracování importu cizích směnných kurzů.

## <a name="configure-an-exchange-rate-provider"></a>Konfigurace poskytovatele směnných kurzů
Než bude možné importovat směnné kurzy, musíte nastavit informace vyžadované zprostředkovateli, kteří nabízejí směnné kurzy. Pomocí stránky **Konfigurace zprostředkovatelů směnného kurzu** vyberte poskytovatele směnných kurzů. Někteří poskytovatelé směnných kurzů jsou zahrnuti v demo datech aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Ovládací prvky tohoto formuláře jsou popsány na následující stránce.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pole** | **Popis**                                                                                                                                                                                                             |
| **Název**  | Název poskytovatele směnného kurzu.                                                                                                                                                                                     |
| **Klíč**   | Jedinečný identifikátor součásti všech konfiguračních informací požadovaný poskytovatelem. Tyto údaje jsou automaticky přidány pro každého poskytovatele směnného kurzu, kterého přidáte klepnutím na tlačítko **Přidat**. |
| **Hodnota** | Informace pro každý klíč. Tyto údaje jsou přidány pro každého poskytovatele směnného kurzu, kterého přidáte klepnutím na tlačítko **Přidat**.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Importovat směnné kurzy měn
Směnné kurzy můžete importovat ze zdroje poskytovatelů směnných kurzů a nastavit je na stránce **Směnné kurzy měn**. Použijte stránku **Importovat směnné kurzy měn**, chcete-li importovat směnné kurzy. Následující tabulka obsahuje popis polí požadovaných k dokončení procesu importu.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pole**                              | **Popis**                                                                                                                                                                                                                                                                                                                                                             |
| **Typ směnného kurzu**                 | Typ směnného kurzu.                                                                                                                                                                                                                                                                                                                                                      |
| **Poskytovatel směnného kurzu**             | Poskytovatel směnného kurzu.                                                                                                                                                                                                                                                                                                                                                  |
| **Importovat jako**                       | Tento parametr řídí, zda mají být importovány k dnešnímu datu nebo období. Pokud chcete použít rozsah dat, zadejte nebo vyberte počáteční a koncové datum.                                                                                                                                                                                                                |
| **Vytvořit nezbytné páry měn**    | Toto zaškrtávací políčko řídí automatické vytváření dvojic měn, pokud neexistují páry měn, které jsou importovány. Tato možnost nemusí být k dispozici pro některé poskytovatele.                                                                                                                                                                                               |
| **Přepsat existující směnné kurzy**   | Toto zaškrtávací políčko spravuje aktualizace stávajícího směnného kurzu pro dvojici měn, když směnný kurz k určitému datu již existuje. Pokud toto políčko nezaškrtnete, směnný kurz pro konkrétní data není importován, pokud již existuje jiný směnný kurz.                                                                                       |
| **Zabránit importu v den státního svátku** | Toto zaškrtávací políčko řídí import směnného kurzu k datu, které připadá na státní svátek. Například pokud vyberte toto zaškrtávací políčko a použijete jako poskytovatele směnného kurzu Evropské centrální banky, systém nebude aktualizovat směnný kurz ve svátek vztahující se k aktuální právnické osobě. Tato možnost nemusí být k dispozici pro některé poskytovatele. |






