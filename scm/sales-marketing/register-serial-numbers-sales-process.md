---
title: "Registrace sériových čísel v prodejním procesu"
description: "Tento článek vysvětluje, jak lze registrovat sériová čísla v dodacích listech nebo fakturách během prodejního procesu. Tato funkce je užitečná, pokud mnoho společností chce jednoduše zaznamenat sériová čísla pro účely záruky a služeb, a nepotřebuje udržovat sériová čísla v zásobách od příjmu po vydání."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: ffb567c0ba9c95d059e64e24cbe0ea53ec9f7bc9
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017


---

# <a name="register-serial-numbers-in-the-sales-process"></a>Registrace sériových čísel v prodejním procesu

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Tento článek vysvětluje, jak lze registrovat sériová čísla v dodacích listech nebo fakturách během prodejního procesu. Tato funkce je užitečná, pokud mnoho společností chce jednoduše zaznamenat sériová čísla pro účely záruky a služeb, a nepotřebuje udržovat sériová čísla v zásobách od příjmu po vydání.

Mnoho společností chce jednoduše zaznamenat sériová čísla pro účely záruky a služeb, a nepotřebuje udržovat sériová čísla v zásobách od příjmu po vydání. V těchto situacích aplikace Microsoft Dynamics 365 for Finance and Operations umožní registrovat sériová čísla v dodacích listech nebo fakturách při prodeji produktu. Při pozdějším vrácení produktu lze trasovat produkt k faktuře k určení, zda jste produkt prodali a zda jsou služby nebo záruční povinnosti platné.
Jsou nějaké požadavky?
----------------------------

Je nutné povolit sériová čísla pro prodejní proces ve skupině sledovací dimenze výběrem možnosti **Aktivní v prodejním procesu** na stránce **Sledování – skupiny dimenze**. V aplikaci Microsoft Dynamics 365 for Finance and Operations pak dojde k následujícím událostem:
-   Na pevné kartě **Sériová čísla** se vybere možnost **Kontrola sériového čísla**. Je-li tato možnost vybrána, je nutné zaregistrovat jedno sériové číslo pro každou položku dodacího listu nebo faktury.
-   Všechny vybrané položky ve skupině sledovací dimenze pro sériová čísla jsou prázdná s výjimkou možnosti **Povolen prázdný výdej**. Můžete vybrat možnost **Povolen prázdný výdej** pro obejití kontroly sériového čísla a povolit produktům balení a fakturaci bez registrace sériových čísel.

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a>Kdy zaregistruju sériová čísla v prodejním procesu?
Registrovat sériová čísla můžete na dodacím listu prodejní objednávky nebo na faktuře. Při přípravě faktury serializovanou položku dodávané společně s dodacím listem můžete vybrat, která sériová čísla dodacího listu vyfakturovat. Počet zaregistrovaných sériových čísel nesmí překročit množství dodávaných položek. Pokud vytváříte dílčí fakturu, můžete vybrat méně serializovaných položek, než bylo zaregistrováno na dodacím listu. Při tisku dodacího listu nebo faktury budou zahrnuta sériová čísla, které byla zaregistrována.

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a>Mohu zadat sériová čísla jejich naskenováním nebo je musím zadávat ručně?
Můžete naskenovat nebo zadat sériová čísla. Při použití skeneru režim skenování určuje, zda se bude přidávat nebo odebírat sériová čísla ze seznamu sériových čísel na faktuře nebo dodacím listu. Pokud chcete skenovat sériová čísla, například pomocí ručního snímače čárového kódu, nastavte skener, aby odesílal příkaz Enter nebo TAB po sériovém čísle. Tento příkaz bude znamenat konec proudu dat. Jinak je nutné stisknout Enter nebo TAB na klávesnici po naskenování každého sériového čísla.

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a>Pokud povolím sériová čísla pro prodejní proces, je nutné zaregistrovat všechna sériová čísla pro všechny položky?
Nastavení pro skupinu sledování dimenze, která je přiřazena k produktu určuje, zda je registrace sériových čísel nutná pro všechny položky na dodacím listu nebo faktuře. Pokud povolíte sériová čísla pro prodejní proces, možnost **Kontrola sériového čísla** se vybere automaticky. Následně je nutné registrovat jedno sériové číslo nebo zaregistrovat prázdnou registraci pro nečitelné číslo pro každou položku dodacího listu nebo faktury. Pokud nechcete požadovat sériové číslo pro každou položku, vyberte možnost **Povolen prázdný výdej** ve skupině sledování dimenze, která je přiřazena k položce. Poté můžete zaregistrovat méně sériových čísel, než je množství položek, které jsou právě dodány. Pokud zaregistrujete více sériových čísel než je množství dodávaných položek, nebudete moci zaúčtovat dodací list nebo fakturu.

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a>Moh zaregistrovat sériová čísla pro dílčí faktury a částečné dodávky?
Můžete vytvořit dílčí faktury a dodací listy pro prodejní objednávky a zaregistrovat sériová pouze čísla položek, které tyto faktury a dodací listy obsahují. Pokud chcete vytvořit dílčí fakturu a máte více než jeden dodací list pro prodejní objednávku, můžete vytvořit sériová čísla z více než jednoho dodacího listu. Může však existovat pouze jeden dodací list, kde nejsou uvedena žádná sériová čísla. Například pokud máte tři dodací listy a každý dodací list obsahuje dvě serializované položky, nelze vytvořit dílčí fakturu pro jednu položku z každého dodacího listu.

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a>Co dělat, když je sériové číslo nečitelné?
Jestliže sériové číslo nelze přečíst nebo skenovat, můžete vytvořit prázdný řádek pro položku klepnutím na tlačítko **Nečitelné** na stránce **Sériová čísla**. Jakmile pořadové číslo bude k dispozici později, můžete aktualizovat fakturu nebo dodací list. Další informace naleznete v části "Je možné opravit nebo změnit sériová čísla, která jsou zaregistrována pro prodejní objednávku?".

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a>Mohu opravit nebo změnit sériová čísla registrovaná pro prodejní objednávku?
Ano, sériová čísla můžete opravit, pokud jsou splněny následující podmínky:
-   **Faktury** - můžete změnit sériová čísla položek, které dosud nebyly vyfakturovány. Dodací list se také aktualizuje. Pokud však byl řádek prodejní objednávky opraven registrací záporného množství, nelze změnit sériová čísla pro řádek prodejní objednávky.
-   **Dodací listy** - nelze částečně opravit řádek dodacího listu, který obsahuje serializované položky. Je nutné stornovat celé množství na řádku. Pokud byl stornován nebo opraven dodací list, není třeba registrovat stornovaná sériová čísla znovu při vytváření nového dodacího listu pro stejné serializované položky. Použijí se čísla, která byla zaregistrována.

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a>Mohu zobrazit sériová čísla, která byla dodána společně s konkrétním dodacím list nebo byla zahrnuta do faktury?
Ano, můžete spustit dotaz na řádek deníku dodacího listu nebo řádek deníku faktury k zobrazení seznamu všech sériových čísel, které byly zahrnuty do dokumentu.

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a>Mohu zobrazit serializované položky, které jsou na skladě?
Ne, nelze zobrazit serializované položky, které máte na skladě, protože sériová čísla nejsou zaregistrována pro položky, dokud se položky neprodají.

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a>Mohu zaregistrovat sériová čísla pro položky se skutečnou hmotností?
Ne, v prodejním procesu nemůžete registrovat sériová čísla pro položky skutečné hmotnosti. Dále pokud je produkt nastaven jako položka skutečné hmotnosti, nelze produkt přiřadit do skupiny sledovací dimenze, která je nastavena pro použití sériových čísel pouze během prodejního procesu.
Je možné registrovat sériová čísla v maloobchodním pokladním systému?
------------------------------------------------

Ano, maloobchodní pokladních systém (POS) vyzve uživatele k zadání sériového čísla, když uživatel prodává položku, které je přiřazena skupina sledovacích dimenzí, která je nastavena na použití sériových čísel pouze během prodejního procesu.

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a>Jaké role zabezpečení jsou nutné k registrování sériových čísel během prodejního procesu?
Tato funkce je k dispozici pro všechny role, které mohou spravovat prodejní dodací listy a prodejní faktury. Následující úkoly umožňují pracovníkům opravit sériová čísla a registrovat prázdné položky registru pro sériová čísla, která nelze přečíst nebo naskenovat:
-   Udržovat opravy sériových čísel
-   Udržovat registraci nečitelných sériových čísel






