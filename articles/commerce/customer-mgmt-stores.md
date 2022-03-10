---
title: Správa zákazníků v obchodech
description: Toto téma vysvětluje, jak mohou maloobchodníci povolit funkce správy zákazníků v místě prodeje (POS) v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 29e45419f712e25092b473e34144ac1146e4ed9b
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913619"
---
# <a name="customer-management-in-stores"></a>Správa zákazníků v obchodech

[!include [banner](includes/banner.md)]

Toto téma vysvětluje, jak mohou maloobchodníci povolit funkce správy zákazníků v místě prodeje (POS) v Microsoft Dynamics 365 Commerce.

Je důležité, aby spolupracovníci obchodu mohli vytvářet a upravovat záznamy zákazníků na POS. Tímto způsobem mohou zaznamenávat jakékoli aktualizace informací o zákaznících, jako je e-mailová adresa, telefonní číslo a adresa. Tyto informace jsou užitečné v následných systémech, jako je marketing, protože účinnost těchto systémů závisí na přesnosti jejich údajů o zákaznících.

Pracovníci prodeje mohou spustit pracovní postup vytváření zákazníků ze dvou vstupních bodů POS. Mohou vybrat tlačítko, které je namapováno na operaci **Přidat zákazníka** nebo mohou vybrat **Vytvořit zákazníka** na panelu aplikací na stránce s výsledky vyhledávání. V obou případech se zobrazí dialogové okno **Nový zákazník**, kde prodejní spolupracovníci mohou zadat požadované údaje o zákazníkovi, například jméno zákazníka, e-mailovou adresu, telefonní číslo, adresu a jakékoli další informace, které jsou relevantní pro danou firmu. Tyto další informace lze zachytit pomocí atributů zákazníka, které jsou spojeny se zákazníkem. Další informace o atributech zákazníka najdete v části [Atributy zákazníka](dev-itpro/customer-attributes.md).

Obchodní spolupracovníci mohou také zaznamenávat sekundární e-mailové adresy a telefonní čísla. Kromě toho mohou zachytit preference zákazníka ohledně přijímání marketingových informací prostřednictvím kterékoli z těchto sekundárních e-mailových adres nebo telefonních čísel. K aktivaci této funkce musí maloobchodníci zapnout funkci **Zaznamenat více e-mailů a telefonních čísel a souhlas s marketingem těchto kontaktů** v pracovním prostoru **Správa funkcí** v centrále Commerce (**Správa systémů \> Pracovní prostory \> Správa funkcí**).

## <a name="default-customer-properties"></a>Výchozí vlastnosti zákazníka

Maloobchodníci mohou použít stránku **Všechny obchody** v ústředí Commerce (**Retail a Commerce \> Kanály \> Obchody**) a přidružit výchozího zákazníka ke každému obchodu. Commerce poté zkopíruje vlastnosti definované pro výchozího zákazníka do všech nových záznamů o zákazníkovi, které jsou vytvořeny. Například dialogové okno **Vytvořit zákazníka** zobrazuje vlastnosti, které jsou zděděny od výchozího zákazníka, který je přidružen k obchodu. Mezi tyto vlastnosti patří **typ zákazníka**, **skupina zákazníků**, **možnost účtenky**, **e-mail příjemce**, **měna** a **jazyk**. Jakékoli **přidružení** (seskupení zákazníků) se dědí také od výchozího zákazníka. **Finanční dimenze** se však dědí ze skupiny zákazníků, která je přidružena k výchozímu zákazníkovi, nikoli od samotného výchozího zákazníka.

> [!NOTE]
> Hodnota **e-mailu s účtenkou** se zkopíruje z výchozího zákazníka pouze v případě, že pro nově vytvořené zákazníky není poskytnuto ID e-mailu s potvrzením. To znamená, že pokud je ID výchozího e-mailu k dispozici u výchozího zákazníka, pak všichni zákazníci vytvoření z webu elektronického obchodování obdrží stejné ID e-mailové účtenky, protože neexistuje žádné uživatelské rozhraní, které by od zákazníka zachytilo ID e-mailu s účtenkou. Doporučujeme vám ponechat pole **e-mail s účtenkou** prázdné pro výchozího zákazníka obchodu a použít jej pouze v případě, že máte obchodní proces, který závisí na přítomné e-mailové adrese s účtenkou. 

Prodejní spolupracovníci mohou pro zákazníka zachytit více adres. Jméno a telefonní číslo zákazníka se dědí z kontaktních informací, které jsou spojeny s každou adresou. Karta s náhledem **Adresy** záznamu zákazníka obsahuje pole **Účel**, které mohou prodejní spolupracovníci upravit. Pokud je typ zákazníka **Osoba**, výchozí hodnota je **Domov**. Pokud je typ zákazníka **Organizace**, výchozí hodnota je **Sídlo**. Mezi další hodnoty, které toto pole podporuje, patří **Domov**, **Kancelář** a **Poštovní schránka**. Hodnota pole **Země** pro adresu je zděděna z primární adresy, která je uvedena na stránce **Provozní jednotka** stránka v centrále Commerce v nabídce **Správa organizace \> Organizace \> Provozní jednotky**.



## <a name="additional-resources"></a>Další prostředky

[Asynchronní režim vytváření zákazníka](async-customer-mode.md)

[Převedení asynchronních zákazníků na synchronní zákazníky](convert-async-to-sync.md)

[Atributy odběratele](dev-itpro/customer-attributes.md)

[Vyloučení dat offline](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
