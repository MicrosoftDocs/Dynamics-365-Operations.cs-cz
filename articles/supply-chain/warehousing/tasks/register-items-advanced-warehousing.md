---
title: Registrace položek pro položky umožňující pokročilé uskladnění s použitím deníku doručení zboží
description: Tento postup popisuje, jak zaregistrovat položky pomocí deníku doručení položek, když použijete pokročilé postupy řízení skladu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f8c39ade92b80c561c9e96220a59e7f222d77e6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216981"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Registrace položek pro položky umožňující pokročilé uskladnění s použitím deníku doručení zboží

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak zaregistrovat položky pomocí deníku doručení položek, když použijete pokročilé postupy řízení skladu. To obvykle provádí přijímající pracovník. 

Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Před zahájením tohoto průvodce musíte mít potvrzenou nákupní objednávku s otevřeným řádkem nákupní objednávky. Položky na řádku musí být na skladě a nesmí používat varianty produktu a nesmí obsahovat sledovací dimenze. Položka zároveň musí být přidružena ke skupině dimenzí úložiště, kde jsou aktivní postupy řízení skladu. Sklad, který se používá, musí být povolen pro procesy správy skladu a umístění, které používáte pro příjem, musí být řízeno registrační značkou. V případě, že používáte USMF, můžete k vytvoření nákupní objednávky použít účet společnosti 1001, sklad 51 a položku M9200. 

Poznamenejte si číslo nákupní objednávky, kterou vytvoříte, a také si poznamenejte číslo položky a pracoviště, které se používá pro váš řádek nákupní objednávky.


## <a name="create-an-item-arrival-journal-header"></a>Vytvoření záhlaví deníku pro doručení položky
1. Přejděte na Doručení položky.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
    * Pokud používáte data USMF, můžete zadat „WHS“. Pokud používáte jiná data, deník s názvem, který zvolíte, musí mít následující vlastnosti: u možnosti Zkontrolovat výdejní skl. místo musí být nastavena hodnota Ne a u Řízení karantény musí být nastavena hodnota Ne.  
4. Zadejte hodnotu do pole Číslo.
5. Zadejte hodnotu do pole Pracoviště.
    * Vyberte pracoviště, které jste používali pro na řádek nákupní objednávky. To bude sloužit jako výchozí hodnota, která bude výchozí pro všechny řádky v deníku. Pokud jste použili sklad 51 USMF, zvolte pracoviště 5.  
6. Zadejte hodnotu do pole Sklad.
    * Vyberte platný sklad pro pracoviště, které jste vybrali. To bude sloužit jako výchozí hodnota, která bude výchozí pro všechny řádky v deníku. Používáte-li například hodnoty v USMF, vyberte 51.  
7. Zadejte hodnotu do pole Místo konání.
    * Vyberte platné umístění ve skladu, který jste vybrali. Skladové místo musí být přiděleno k profilu skladového místa, které je řízeno registrační značkou. To bude sloužit jako výchozí hodnota, která bude výchozí pro všechny řádky v deníku. Používáte-li například hodnoty v USMF, vyberte Bulk-008.  
8. Klepněte pravým tlačítkem myši na šipku rozevíracího seznamu v poli Registrační značka, a pak vyberte možnost Zobrazit podrobnosti.
9. Klikněte na položku Nová.
10. V poli Registrační značka zadejte hodnotu.
    * Poznamenejte si hodnoty.  
11. Klikněte na položku Uložit.
12. Zavřete stránku.
13. V poli Registrační značka zadejte hodnotu.
    * Zadejte hodnotu registrační značky, kterou jste právě vytvořili. To bude sloužit jako výchozí hodnota, která bude výchozí pro všechny řádky v deníku.  
14. Klikněte na tlačítko OK.

## <a name="add-a-line"></a>Přidání řádku
1. Klikněte na položku Přidat řádek.
2. Zadejte hodnotu do pole Číslo zboží.
    * Zadejte číslo položky, která je použita na řádku nákupní objednávky.  
3. Zadejte číslo do pole Množství.
    * Zadejte množství, které chcete registrovat.  
    * Pole Datum určuje datum, kdy bude na skladě registrováno množství této položky.  
    * ID šarže bude vyplněno systémem, pokud může být jedinečně identifikováno z uvedených informací. V opačném případě bude nutné ho přidat ručně. Toto je povinné pole, které propojí tuto registraci k řádku konkrétního zdrojového dokumentu.  

## <a name="complete-the-registration"></a>Dokončení registrace
1. Klikněte na tlačítko Ověřit.
    * To kontroluje, zda je deník připraven k zaúčtování. Jestliže se ověření nezdaří, které bude nutné před zaúčtováním deníku opravit chyby.  
2. Klikněte na tlačítko OK.
    * Poté, co jste klepnuli na tlačítko OK, zkontrolujte zprávu. Musí existovat zpráva o tom, že deník je v pořádku.  
3. Klikněte na položku Zaúčtovat.
4. Klikněte na tlačítko OK.
    * Poté, co jste kliknuli na tlačítko OK, zkontrolujte pruh zpráv. Musí existovat zpráva o tom, že operace byla dokončena.  
5. Zavřete stránku.

