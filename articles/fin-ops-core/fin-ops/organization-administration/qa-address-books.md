---
title: Často kladené dotazy k adresářům
description: Tento článek obsahuje odpovědi na časté dotazy související s adresáři.
author: msftbrking
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirPartyCheckDuplicate, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23601
ms.assetid: b177fa0f-ac9a-415e-9498-15438e132f60
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b7262bc0be5330ac239fbceff96108477e2a796
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881015"
---
# <a name="address-books-faq"></a>Často kladené dotazy o adresáři

[!include [banner](../includes/banner.md)]

## <a name="how-do-i-check-for-duplicate-records"></a>Jak zkontroluji duplicitní záznamy?

Je možné kontrolovat duplicitní záznamy přímo na stránce seznamu **Globální adresář**. Na panelu akcí na kartě **Strana** ve skupině **Spravovat** klikněte na možnost **Kontrolovat duplicity**. Poté vyberte hodnoty k zahrnutí do kontroly duplicit.

## <a name="can-i-bulk-add-or-delete-party-records-from-an-address-book"></a>Je možné hromadně přidat nebo odstranit záznamy strany z adresáře?

Ano, můžete přidat několik záznamů strany do adresáři a také odstranit několik záznamů strany.

- Chcete-li přidat více záznamů strany do adresáře, na stránce seznamu **Globální adresář** vyberte ze seznamu strany. Poté na panelu akcí na kartě **Strana** ve skupině **Spravovat** klikněte na možnost **Přiřadit strany**. Vyberte adresáře, do kterých chcete přidat vybrané záznamy strany, a klikněte na tlačítko **OK**. Všechny vybrané záznamy strany jsou přidány do vybraných adresářů.
- Chcete-li odebrat více záznamů strany z adresáře, na stránce seznamu **Globální adresář** vyberte ze seznamu strany. Poté na panelu akcí na kartě **Strana** ve skupině **Spravovat** klikněte na možnost **Odebrat strany**. Vyberte adresáře, ze kterých chcete odebrat strany, a potom klikněte na tlačítko **OK**. Všechny vybrané záznamy strany budou odebrány z vybraných adresářů.

## <a name="can-i-change-the-party-type-of-a-record-or-do-i-have-to-delete-the-old-record-and-create-a-new-one"></a>Mohu změnit typ strany záznamu nebo je nutné odstranit původní záznam a vytvořit nový?

V některých případech je třeba změnit typ strany záznamu z osoby na organizaci nebo z organizace na osobu. Například Anna je členem prodejního týmu společnosti Fabrikam U.K. Na veletrhu v Londýně se setká se šesti novými potenciálními zákazníky. Anna vytvoří záznam strany potenciálního zákazníka pro každého potenciálního zákazníka. Když Anna uloží záznamy, jsou všechny záznamy rovněž vytvořeny v globálním adresáři. Společnost Fabrikam má nastaven výchozí typ strany na organizaci, ale dva noví potenciální zákazníci by měli mít typ záznamu "osoba". Proto když se Anna z veletrhu vrátí, musí změnit typ strany záznamu dvou potenciálních zákazníků. Chcete-li změnit záznam strany na jiný typ, musíte nejprve vytvořit nový záznam strany správného typu v globálním adresáři. Poté můžete přidružit původní záznam strany k tomuto novému záznamu. Po provedení nového přidružení strany odstraňte původní záznam strany, který má nesprávný typ záznamu.

## <a name="how-do-i-change-the-name-or-address-of-a-party-record"></a>Jak změním název nebo adresu záznamu strany?

Název záznamu strany a adresy, které jsou přiřazeny k tomuto záznamu, lze kdykoli aktualizovat.

- Pokud chcete aktualizovat název záznamu strany, otevřete záznam strany a v podokně akcí klikněte na tlačítko **Upravit**. Na pevné záložce **Obecné** zadejte nový název strany a poté záznam uložte.
- Chcete-li aktualizovat adresu pro záznam strany, otevřete záznam strany a poté na pevné záložce **Adresy** vyberte adresu, kterou chcete aktualizovat. Klikněte na tlačítko **Upravit** a poté na stránce **Upravit adresu** proveďte požadované změny adresy nebo parametrů adresy.

## <a name="can-i-merge-two-or-more-party-records-into-one-record"></a>Mohu do jednoho záznamu sloučit dva nebo více záznamů strany?

V některých případech můžete chtít sloučit dvou nebo více záznamů strany do jednoho záznamu. K tomu může dojít při vytvoření jednoho nebo několika duplicitních záznamů strany – záměrně nebo neúmyslně. Při sloučení záznamů strany vyberete jeden záznam, který ponecháte. Informace z jiných záznamů se poté sloučí do tohoto záznamu. Například zjistíte že informace o společnosti Fabrikam jsou uloženy ve třech záznamech strany: A, B a C. Rozhodnete se zachovat záznam strany A. Proto budou informace, které jsou uloženy v záznamech strany B a C, sloučeny do záznamu strany A. Existuje několik situacích, kdy nelze záznamy strany sloučit:

- Nelze sloučit záznamy strany přidružené ke stejné roli strany, jako je například odběratel nebo dodavatel, ve stejné právnické osobě. Například strana A je přidružena k odběrateli v právnické osobě 123 a strana B je přidružen k jinému zákazníkovi v právnické osobě 123. Tyto záznamy strany nelze sloučit, protože kdyby byly sloučeny, záznam sloučené strany by byl přidružený k více zákazníkům ve stejné právnické osobě, což není povoleno. Záznamy lze však sloučit, pokud je strana B přiřazená dodavateli v právnické osobě 123 nebo odběrateli v jiné právnické osobě.
- Nelze sloučit interní záznamy organizace strany ve stejné právnické osobě, týmu nebo provozní jednotce.

## <a name="should-i-create-a-party-record-in-the-global-address-book-or-in-another-place-such-as-the-customer-or-vendor-page"></a>Mám vytvořit záznam strany v globálním adresáři nebo na jiném místě, například na stránce odběratele nebo dodavatele?

Můžete zadat záznamy strany buď v globálním adresáři nebo na stránce příslušné entity. Přidáte-li záznam na jednom místě, bude stejný záznam vždy přidán do jiného umístění. Například pokud přidáte záznam strany pro odběratele do globálního adresáře, bude tento záznam přidán také na stránku **Odběratel**. Podobně pokud přidáte záznam strany pro odběratele na stránku **Odběratel**, bude tento záznam přidán také do globálního adresáře. Na základě následujících pokynů rozhodněte, kam byste měli zadat nové záznamy strany:

- **Vytvoření záznamu strany, když neznáte typ entity** – Pokud musíte vytvořit záznam strany, ale neznáte typ entity (například nevíte, zda je entita odběratel nebo příležitost), vytvořte záznam v globálním adresáři. Typ entity můžete vybrat později.
- **Vytvoření záznamu strany, když znáte typ entity** – Pokud znáte typ entity strany, můžete vytvořit záznam na příslušné stránce pro tento typ. Například vytvořte záznam pro odběratele na stránce **Odběratel**. Při vytvoření a uložení záznamu pomocí stránky příslušné entity, bude záznam automaticky vytvořen v globálním adresáři.

## <a name="can-i-translate-address-information-for-party-records"></a>Mohu převést informace o adrese pro záznamy strany?

Můžete nastavit překlady informací o adrese, aby se tyto údaje zobrazily ve vašem uživatelském jazyce (systémový jazyk) ve vaší aplikaci, ale v jiném jazyce v dokumentech, jako například prodejních objednávkách. Je možné zadat překlady pro názvy zemí nebo oblastí, adresy a pořadí jmen. Například váš systémový jazyk je dánština a vytváříte prodejní objednávku pro odběratele ve Francii. V takovém případě lze zobrazit záznam odběratele v dánštině v programu, ale informace o adrese zobrazit ve francouzštině v tištěné prodejní objednávce. Při nastavování překladů měli byste zadat překlad pro všechny položky v seznamu. Všechny položky, pro které nezadáte překlad, se zobrazí v systémovém jazyce. Například váš systémový jazyk je dánština a odesíláte dokument odběrateli ve Francii. Pokud jste nezadali překlady pro španělštinu (ESP) pro adresní údaje, příslušné informace se zobrazí v dánštině v programu i ve vytištěném dokumentu.

## <a name="after-i-import-addresses-why-cant-i-edit-the-records"></a>Proč nemohu po importu adres upravit záznamy?

Při importu adres je pole s názvem **IsLocationOwner**. Toto pole udává, zda strana, která je spojena s místem (adresou), je vlastníkem adresy. Pokud je strana vlastníkem adresy, lze adresu upravit při použití strany v globálním adresáři nebo z formuláře hlavního záznamu (například zákazník, prodejce nebo pracovník). Pokud strana není vlastníkem adresy, záznam nelze upravit. 

Při importu adres by mělo pole **IsLocationOwner** být nastaveno na **Ano**, chcete-li adresu upravit pomocí přidružené strany. Pokud je toto pole importováno nesprávně, vlastníka umístění lze aktualizovat v globálním adresáři.

Další informace o tom, jak změnit vlastníka umístění importované adresy, najdete v tématu [Správa vlastníků lokality](./global-address-book-location-owner.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
