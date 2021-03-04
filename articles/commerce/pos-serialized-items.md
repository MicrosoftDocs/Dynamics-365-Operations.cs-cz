---
title: Práce se serializovanými položkami v POS
description: Toto téma vysvětluje, jak spravovat serializované položky v aplikaci pokladního místa (POS).
author: boycezhu
manager: annbe
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 6ba01abc3d1a4496ec586a621aa03b4981f84d76
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410896"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Práce se serializovanými položkami v POS

[!include [banner](includes/banner.md)]

Mnoho prodejců prodává výrobky, které vyžadují sériovou kontrolu. Tyto produkty jsou označovány jako *serializované položky*. Někteří prodejci mohou chtít udržovat sériová čísla zásob v obchodě nebo skladu pro účely sledování. Ostatní prodejci mohou chtít během procesu prodeje zachytit sériová čísla pro účely servisu a záruky. Toto téma vysvětluje, jak můžete spravovat serializované položky v aplikaci pokladního místa (POS) Microsoft Dynamics 365 Commerce.

## <a name="serial-number-configurations"></a>Konfigurace sériového čísla

Položka je považována za serializovanou položku, pokud jí je přiřazena skupina sledovacích dimenzí, která je nastavena tak, aby umožňovala sériová čísla. V centrále Commerce na stránce **Skupiny sledovací dimenze** vyberte volbu **Aktivní** pro povolení sériových čísel pro proces zásob nebo volbu **Aktivní v prodejním procesu** pro povolení sériových čísel pro prodejní proces.

Na záložce s náhledem **Sledovací dimenze** zapněte parametr **Povolen příjem prázdných hodnot**, kterým povolíte, že během procesu příjmu zásob serializované položky bude sériové číslo volitelným vstupem. Vypnutí tohoto parametru vynutí sériové číslo jako povinný vstup. Podobně parametr **Povolen prázdný výdej** určuje, zda je během procesu expedice zásob vyžadováno sériové číslo.

> [!NOTE]
> Pokud chcete pomocí operací POS **Příchozí zásoby** a **Odchozí zásoby** zaregistrovat nebo ověřit sériová čísla se serializovanou položkou, musíte tuto položku nakonfigurovat tak, aby byla přiřazena skupině sledovací dimenze, která je nastavena tak, aby umožňovala sériová čísla pro možnost **Aktivní** namísto možnosti **Aktivní v prodejním procesu**.

## <a name="serial-number-management-page"></a>Stránka správy sériového čísla

V operacích POS **Příchozí zásoby** a **Odchozí zásoby**, pokud je položka, která je vybrána, přijata nebo odeslána, serializovanou položkou, podokno **Podrobnosti** obsahuje možnost **Spravovat sériové číslo**, která odkazuje na stránku **Správa sériového čísla**, kde můžete zaregistrovat nebo ověřit sériová čísla položky. Případně můžete stránku **Správa sériových čísel** otevřít buď výběrem akce **Sériové číslo** na panelu aplikací v zobrazení podrobností objednávky nebo výběrem možnosti **Spravovat sériové číslo** v dialogovém okně, které vás vyzve během procesu příjmu nebo expedice. 

Stránka **Správa sériových čísel** obsahuje seznam všech otevřených řádků sériového čísla, které čekají na registraci nebo ověření. Na této stránce mohou být dvě karty: jedna pro aktuální položku a druhá pro všechny serializované položky v pořadí.

Pole **Stav** na stránce **Správa sériových čísel** stránka poskytuje informace o aktuální fázi, v níž je každé sériové číslo:

- **Neregistrováno** - Sériové číslo nebylo zadáno, nebo dosud zaregistrované sériové číslo nebylo ověřeno (během procesu příjmu).
- **Registrace** - Sériové číslo bylo registrováno a uloženo lokálně do databáze kanálů v obchodě nebo bylo ověřeno předem zaregistrované sériové číslo. Pouze sériová čísla, která mají stav **Probíhá registrace** budou po dokončení příjmu nebo plnění odeslána do centrály Commerce.

## <a name="receive-serialized-items"></a>Příjem serializovaných položek

Operace POS **Příchozí zásoby** umožňuje uživatelům provádět následující úkoly pro serializované položky:

- Registrace sériových čísel proti serializovaným položkám, když jsou tyto položky v obchodě přijaty prostřednictvím objednávky.
- Ověření předem registrovaných sériových čísel proti serializovaným položkám, když jsou tyto položky v obchodě přijaty prostřednictvím nákupní objednávky nebo příkazu pro převod.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrace sériových čísel proti serializovaným položkám

Pro nákupní objednávku se vám zobrazí dialogové okno s možností **Spravovat sériové číslo** během procesu přijímání serializované položky. Tuto možnost můžete vybrat, aby se otevřela stránka **Správa sériových čísel**, a začít registrovat sériová čísla. Tento krok můžete také přeskočit během procesu příjmu a zadat vstup později, předtím, než bude příjem zaúčtován.

Ve výchozím nastavení je zobrazena karta pro aktuální položku. Všechny řádky sériového čísla mají prázdnou hodnotu sériového čísla a stav **Neregistrovaný**. Můžete naskenovat čárové kódy sériového čísla, nebo můžete vybrat **Sériové číslo** na panelu aplikace, abyste průběžně zadávali sériová čísla. Sériová čísla, která zadáte, se objeví v seznamu a jejich stav se změní na **Registrace**. Maximální počet sériových čísel, která můžete zaregistrovat v seznamu, se rovná přijímanému množství. Pokud uděláte chybu, můžete vybrat **Upravit** nebo **Vymazat** v podokně **Podrobnosti** a provést změny zadaných sériových čísel.

Můžete také zaregistrovat sériová čísla na kartě **Všechny serializované položky** na stránce **Správa sériových čísel**. V seznamu vyberte položku, pro kterou chcete zaregistrovat sériová čísla.

### <a name="validate-serial-numbers-on-serialized-items"></a>Ověření sériových čísel u serializovaných položek

V případě převodu musí odchozí strana předběžně zaregistrovat sériová čísla serializovaných položek během procesu dodávky. V případě objednávky může dodavatel poskytnout informace o sériovém čísle prostřednictvím předběžného oznámení o odeslání (ASN) a vy můžete předregistrovat čísla u položek, které budou odeslány. V obou případech jsou sériová čísla známá před přijetím. Proto na příchozí straně musíte pouze potvrdit, že jste obdrželi to, co jste měli přijmout.

Chcete-li ověřit sériová čísla, můžete otevřít stránku **Správa sériových čísel** buď během procesu příjmu, nebo kdykoli před zaúčtováním příjmu. Pro každou sériovou položku, která má předregistrovaná sériová čísla, jsou všechna sériová čísla na této stránce automaticky nastavena na výchozí stav **Neregistrovaný**. Chcete-li ověřit sériová čísla, můžete je naskenovat nebo zadat. Po zadání sériového čísla aplikace ověří, zda odpovídají předem zaregistrovaným sériovým číslům. Pokud se shodují, jejich stav se změní na **Registrace**. Jinak dostanete chybovou zprávu. Případně můžete přímo vybrat sériové číslo a poté vybrat možnost **Ověřit sériové číslo** v podokně **Podrobnosti** pro rychlé označení tohoto sériového čísla jako ověřeného. Maximální počet sériových čísel, která můžete v seznamu ověřit, se rovná přijímanému množství.

Můžete také ověřit sériová čísla na kartě **Všechny serializované položky** na stránce **Správa sériových čísel**. V seznamu vyberte položku, pro kterou chcete ověřit sériová čísla.

## <a name="ship-serialized-items"></a>Expedice serializovaných položek

Můžete použít operaci POS **Odchozí zásoby** k registraci sériových čísel pro serializované položky při jejich expedici z aktuálního obchodu prostřednictvím převodního příkazu.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrace sériových čísel proti serializovaným položkám

Pro převodní příkaz se vám zobrazí dialogové okno s možností **Spravovat sériové číslo** během procesu expedice serializované položky. Tuto možnost můžete vybrat, aby se otevřela stránka **Správa sériových čísel**, a začít registrovat sériová čísla. Tento krok můžete také přeskočit během procesu expedice a zadat vstup později, předtím, než bude expedice zaúčtována.

Ve výchozím nastavení je zobrazena karta pro aktuální položku. Všechny řádky sériového čísla mají prázdnou hodnotu sériového čísla a stav **Neregistrovaný**. Můžete naskenovat čárové kódy sériového čísla, nebo můžete vybrat **Sériové číslo** na panelu aplikace, abyste průběžně zadávali sériová čísla. Sériová čísla, která zadáte, se objeví v seznamu a jejich stav se změní na **Registrace**. Maximální počet sériových čísel, která můžete zaregistrovat v seznamu, se rovná expedovanému množství. Pokud uděláte chybu, můžete vybrat **Upravit** nebo **Vymazat** v podokně **Podrobnosti** a provést změny zadaných sériových čísel.

Můžete také zaregistrovat sériová čísla na kartě **Všechny serializované položky** na stránce **Správa sériových čísel**. V seznamu vyberte položku, pro kterou chcete zaregistrovat sériová čísla.

Volitelně můžete povolit ověření dostupnosti sériového čísla během registrace sériového čísla na odchozím převodnímu příkazu. Pokud se s tímto ověřením pokusíte odeslat sériové číslo, které není k dispozici v zásobách expedujícího obchodu, obdržíte chybovou zprávu a musíte uvést jiné číslo.

Aby bylo možné takové ověření povolit, je třeba naplánovat, aby se následující úlohy spouštěly opakovaně:

- **Retail a Commerce** > **IT pro Retail a Commerce** > **Produkty a zásoby** > **Dostupnost produktu se sledovacími dimenzemi**
- **Retail a Commerce** > **Plány distribuce** > **1130** (**Dostupnost produktu**)

## <a name="additional-resources"></a>Další prostředky

[Operace příchozích zásob v POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Operace odchozích zásob v POS](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)


[!INCLUDE[footer-include](../includes/footer-banner.md)]