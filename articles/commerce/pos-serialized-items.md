---
title: Práce se serializovanými položkami v POS
description: Toto téma vysvětluje, jak spravovat serializované položky v aplikaci pokladního místa (POS).
author: boycezhu
manager: annbe
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 0431ffa45eceac5c12d8ed991b00730c50ca62f8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972548"
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

## <a name="sell-serialized-items-in-pos"></a>Prodej serializovaných položek v POS

Zatímco aplikace POS vždy podporovala prodej serializovaných položek, v Commerce verze 10.0.17 a novější mohou organizace povolit funkce, které vylepšují obchodní logiku, která se aktivuje při prodeji produktů, které jsou nakonfigurovány pro sledování sériového čísla.

Když je povolena funkce **Vylepšená validace sériového čísla při snímání a plnění objednávek POS**, při prodeji serializovaných produktů v POS se vyhodnotí následující konfigurace produktu:

- Nastavení **Typ sériového čísla** produktu (**aktivní** nebo **aktivní v prodeji**).
- Nastavení **Povolen prázdný výdej** produktu.
- Nastavení **Záporný fyzický sklad** produktu a / nebo prodejního skladu.

### <a name="active-serial-configurations"></a>Konfigurace aktivního sériového čísla

Když se v POS prosávají položky, které jsou konfigurovány s **Aktivní** sledovací dimenzí sériového čísla, POS inicializuje logiku ověřování, která uživatelům brání v dokončení prodeje serializované položky se sériovým číslem, které nelze najít v aktuálních zásobách prodejního skladu. Z tohoto ověřovacího pravidla existují dvě výjimky:

- Pokud je položka také nakonfigurována s povolenou funkcí **Povolen prázdný výdej**, uživatelé mohou přeskočit zadání sériového čísla a prodat položku bez označení sériového čísla.
- Pokud je položka a / nebo prodejní sklad nakonfigurován s povolenou možností **Záporný fyzický sklad**, aplikace přijímá a prodává sériové číslo, u kterého nelze potvrdit, že je v inventáři ve skladu, proti kterému se prodává. Tato konfigurace umožňuje, aby transakce inventáře pro tuto konkrétní položku / sériové číslo byla záporná, a proto systém umožní prodej neznámých sériových čísel.

> [!IMPORTANT]
> Chcete-li zajistit, aby aplikace POS mohla správně ověřit, zda se prodávaná sériová čísla položek s **Aktivním** typem sériového číska nacházejí v zásobách prodejního skladu, je nutné, aby organizace často spouštěly úlohu **Dostupnost produktu se sledovacími dimenzemi** v centrále Commerce a doprovodnou úlohu **1130** distribuce dostupnosti produktů prostřednictvím centrály Commerce. Aby mohla POS ověřit dostupnost zásob prodávaných sériových čísel, když je do prodejních skladů přijímán nový serializovaný inventář, hlavní server zásob často aktualizovat databázi kanálů pomocí nejaktuálnějších údajů o dostupnosti zásob. Úloha **Dostupnost produktu se sledovacími dimenzemi** pořizuje aktuální snímek hlavního inventáře, včetně sériových čísel, pro všechny sklady společnosti. Distribuční úloha **1130** pořídí tento snímek inventáře a sdílí ho se všemi nakonfigurovanými databázemi kanálů.

### <a name="active-in-sales-process-serial-configurations"></a>Aktivní konfigurace sériových čísel v prodejním procesu

Položky konfigurované se sériovou dimenzí jako **Aktivní v procesu prodeje** neprocházejí žádnou logikou ověření zásob, protože tato konfigurace znamená, že sériová čísla zásob nejsou předregistrována do skladu a sériová čísla jsou zachycena pouze v době prodeje.  

Pokud je **Povolen prázdný výdej** také nakonfigurován pro položky **Aktivní v prodejním procesu**, zadání sériového čísla lze přeskočit. Pokud **Povolen prázdný výdej** není nakonfigurován, aplikace vyžaduje, aby uživatel zadal sériové číslo, i když nebude ověřeno podle dostupného inventáře.

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>Při vytváření POS transakcí použijte sériová čísla

Aplikace POS okamžitě vyzve uživatele k zachycení sériového čísla při prodeji serializované položky, ale aplikace umožňuje uživatelům přeskočit zadávání sériových čísel až do určitého bodu procesu prodeje. Když uživatel začne přijímat platby, aplikace vynutí zadání sériového čísla pro všechny položky, které nejsou nakonfigurovány tak, aby byly splněny prostřednictvím budoucích zásilek nebo vyzvednutí. Jakékoli serializované položky nakonfigurované jako cash and carry nebo carryout vyžadují, aby uživatel před dokončením prodeje zadal sériové číslo (nebo souhlasil s tím, že ponechá prázdné, pokud to konfigurace položky umožňuje).

U serializovaných položek prodaných pro budoucí vyzvednutí nebo odeslání mohou uživatelé POS přeskočit zadávání sériového čísla na začátku a přesto dokončit vytvoření objednávky zákazníka.   

> [!NOTE]
> Při prodeji nebo plnění serializovaných produktů prostřednictvím aplikace POS je pro serializované položky v prodejní transakci vynuceno množství „1“. To je výsledek toho, jak jsou informace o sériovém čísle sledovány na prodejní lince. Při prodeji nebo plnění transakce u více serializovaných položek prostřednictvím POS musí být každá prodejní linka nakonfigurována pouze s množstvím „1“. 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>Použijte sériová čísla během plnění nebo vyzvednutí objednávky zákazníka

Při plnění řádků objednávek zákazníků pro serializované produkty pomocí operace **Plnění objednávek** v POS, POS vynucuje zachycení sériového čísla před konečným plněním. Pokud tedy sériové číslo nebylo poskytnuto během počátečního zachycení objednávky, musí být zachyceno během procesu vyzvednutí, zabalení nebo odeslání v POS. Ověření se provádí v každém kroku a uživatel bude požádán o údaje o sériovém čísle, pouze pokud chybí nebo již neplatí. Například pokud uživatel přeskočí kroky vyzvednutí nebo zabalení a okamžitě zahájí dodávku a sériové číslo nebylo pro linku zaregistrováno, POS bude vyžadovat zadání sériového čísla před dokončením posledního kroku faktury. Při vynucování zachycení sériového čísla během operací plnění objednávek v POS stále platí všechna pravidla uvedená dříve v tomto tématu. Pouze serializované položky nakonfigurované jako **Aktivní** projdou ověřením sériového čísla zásob. Položky nakonfigurované jako **Aktivní v procesu prodeje** nebudou ověřeny. Je-li **Záporný fyzický sklad** povolen pro **Aktivní** produkty, bude přijato jakékoli sériové číslo bez ohledu na dostupnost na skladu. Pro **Aktivní** i **Aktivní v procesu prodeje** položky, pokud je nakonfigurován **Povolen prázdný výdej**, může uživatel ponechat sériová čísla prázdná, pokud je to požadováno během kroků vyzvednutí, zabalení a dodání.

Ověření sériových čísel také nastane, když uživatel provede operace vyzvednutí u objednávek zákazníků v POS. Aplikace POS neumožňuje finalizaci vyzvednutí na serializovaném produktu, pokud neprojde validacemi, jak bylo uvedeno výše. Ověření vždy vychází z dimenze sledování produktu a konfigurací prodejního skladu. 

## <a name="additional-resources"></a>Další prostředky

[Operace příchozích zásob v POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Operace odchozích zásob v POS](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)


[!INCLUDE[footer-include](../includes/footer-banner.md)]