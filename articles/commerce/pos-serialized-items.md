---
title: Práce se serializovanými položkami v POS
description: Toto téma vysvětluje, jak spravovat serializované položky v aplikaci pokladního místa (POS).
author: boycezhu
manager: annbe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eedb64ae04345cb94bdd8cc68de833cfcfd40119
ms.sourcegitcommit: 39981582778b0a62567324452485a6721ca18284
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/27/2020
ms.locfileid: "3407491"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Práce se serializovanými položkami v POS

[!include [banner](includes/banner.md)]

Mnoho prodejců prodává výrobky, které vyžadují sériovou kontrolu. Tyto položky jsou označovány jako *serializované položky*. Někteří prodejci mohou chtít udržovat sériová čísla pro účely sledování. Ostatní prodejci mohou chtít během procesu prodeje zachytit sériová čísla pro účely servisu a záruky. Toto téma vysvětluje, jak můžete spravovat serializované položky v aplikaci pokladního místa (POS) Microsoft Dynamics 365 Commerce.

## <a name="serial-number-configurations"></a>Konfigurace sériového čísla

Položka je považována za serializovanou položku, pokud jí je přiřazena skupina sledovacích dimenzí, která je nastavena tak, aby umožňovala sériová čísla. V centrále obchodu na stránce **Sledování skupin dimenzí** vyberte možnost **Aktivní** k povolení sériových čísel pro proces zásob. Chcete-li povolit sériová čísla pro prodejní proces, vyberte možnost **Aktivní v prodejním procesu**.

Pokud je na pevné záložce **Dimenze sledování** zapnutá možnost **Povolen příjem prázdných hodnot**, je během procesu příjmu zásob sériové číslo volitelným vstupem. Pokud je tato volba vypnutá, je vyžadováno sériové číslo.

Pokud je na pevné záložce **Sériová čísla** zapnutá volba **Kontrola sériového čísla**, musí být sériové číslo pro jednotku jedinečné. Jinými slovy, duplikovaná sériová čísla nejsou povolena.

## <a name="serialized-items-in-the-receiving-process"></a>Serializované položky v přijímacím procesu

Operace **Příchozí zásoby** v aplikaci POS umožňuje uživatelům provádět následující úkoly pro serializované položky:

- Registrace sériových čísel proti serializovaným položkám, když jsou tyto položky v obchodě přijaty prostřednictvím objednávky.
- Ověření předem registrovaných sériových čísel proti serializovaným položkám, když jsou tyto položky v obchodě přijaty prostřednictvím nákupní objednávky nebo příkazu pro převod.

> [!NOTE]
> Pokud chcete pomocí operace **Příchozí inventář** zaregistrovat nebo ověřit serializovanou položku, musí být této položce přiřazena skupina sledovací dimenze, která je nastavená tak, aby umožňovala sériová čísla pro možnost **Aktivní**, nikoli možnost **Aktivní v procesu prodeje**.

Chcete-li zahájit proces přijímání, v operaci **Příchozí zásoby** můžete začít v zobrazení **Přijímám nyní** naskenováním čárového kódu položky nebo zadáním ID položky. Případně můžete začít v zobrazení **Úplný seznam objednávek** ručním výběrem položky.

Pokud je položka, která je vybrána nebo přijata, serializovanou položkou, bude podokno **Podrobnosti** dané položky obsahovat odkaz **Spravovat sériové číslo**, který otevře stránku **Správa sériových čísel**. Případně můžete stránku **Správa sériových čísel** otevřít buď výběrem možnosti **Sériové číslo** na panelu aplikací v zobrazení podrobností objednávky nebo výběrem možnosti **Spravovat sériové číslo** v dialogovém okně, které vás během procesu příjmu vyzve. Stránka **Správa sériových čísel** obsahuje seznam všech otevřených řádků sériového čísla, které čekají na registraci nebo ověření. Na této stránce mohou být dvě karty: jedna pro aktuální položku a druhá pro všechny serializované položky v pořadí.

Pole **Stav** na stránce **Správa sériových čísel** stránka poskytuje informace o aktuální fázi, v níž je každé sériové číslo:

- **Neregistrováno** - Sériové číslo nebylo zadáno, nebo dosud zaregistrované sériové číslo nebylo ověřeno.
- **Registrace** - Sériové číslo bylo registrováno a uloženo lokálně do databáze kanálů v obchodě nebo bylo ověřeno předem zaregistrované sériové číslo. Pouze sériová čísla, která mají stav **Probíhá registrace** budou po dokončení příjmu odeslána do centrály obchodu.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrace sériových čísel proti serializovaným položkám

Pro nákupní objednáku nabízí dialogové okno, které vás vyzve během procesu přijímání serializované položky, možnost **Spravovat sériové číslo**. Tuto možnost můžete vybrat, aby se otevřela stránka **Správa sériových čísel**, a začít registrovat sériová čísla. Tento krok můžete také přeskočit během procesu příjmu a zadat vstup později, předtím, než bude příjem zaúčtován.

Ve výchozím nastavení je zobrazena karta pro aktuální položku. Všechny řádky sériového čísla mají prázdnou hodnotu sériového čísla a stav **Neregistrovaný**. Můžete naskenovat čárové kódy sériového čísla, nebo můžete vybrat **Sériové číslo** na panelu aplikace, abyste v dialogovém okně průběžně zadávali sériová čísla. Sériová čísla, která zadáte, se objeví v seznamu a stav řádků sériových čísel se změní na **Registrace**. Maximální počet sériových čísel, která můžete zaregistrovat v seznamu, se rovná přijímanému množství. Pokud uděláte chybu, můžete vybrat **Upravit** nebo **Vymazat** v podokně **Podrobnosti** a provést změny zadaných sériových čísel.

Můžete také zaregistrovat sériová čísla na kartě **Všechny serializované položky** na stránce **Správa sériových čísel**. V seznamu vyberte položku, pro kterou chcete zaregistrovat sériová čísla.

Během registrace sériového čísla na této stránce dochází k ověření duplikace. Pokud se pokusíte zadat duplikované sériové číslo proti položce, pro kterou je zapnuta kontrola sériového čísla, zobrazí se chybová zpráva a musíte zadat jiné číslo.

### <a name="validate-serial-numbers-on-serialized-items"></a>Ověření sériových čísel u serializovaných položek

V případě převodu musí odchozí strana předběžně zaregistrovat sériová čísla serializovaných položek během procesu dodávky. V případě objednávky může dodavatel poskytnout informace o sériovém čísle prostřednictvím předběžného oznámení o odeslání (ASN) a vy můžete předregistrovat čísla u položek, které budou odeslány. V obou případech jsou sériová čísla známá před přijetím. Proto na příchozí straně musíte pouze potvrdit, že jste obdrželi to, co jste měli přijmout.

Chcete-li ověřit sériová čísla, můžete otevřít stránku **Správa sériových čísel** buď během procesu příjmu, nebo kdykoli před zaúčtováním příjmu. Pro každou sériovou položku, která má předregistrovaná sériová čísla, jsou všechna sériová čísla na této stránce automaticky nastavena na výchozí stav **Neregistrovaný**. Chcete-li ověřit sériová čísla, můžete je naskenovat nebo zadat. Po zadání sériového čísla aplikace ověří, zda odpovídají předem zaregistrovaným sériovým číslům. Pokud se shodují, jejich stav se změní na **Registrace**. Jinak dostanete chybovou zprávu. Maximální počet sériových čísel, která můžete v seznamu ověřit, se rovná přijímanému množství.

Můžete také ověřit sériová čísla na kartě **Všechny serializované položky** na stránce **Správa sériových čísel**. V seznamu vyberte položku, pro kterou chcete ověřit sériová čísla.

## <a name="additional-resources"></a>Další prostředky

[Operace příchozích zásob v POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)
