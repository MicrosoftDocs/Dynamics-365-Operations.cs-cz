---
title: Připravenost produktu
description: Toto téma vysvětluje, jak můžete pomocí kontrol připravenosti zajistit, aby byla pro produkt dokončena požadovaná hlavní data před použitím v transakcích.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4286f72f9aed1b4dd91e7c45203cfab2af43f3c2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571946"
---
# <a name="product-readiness"></a>Připravenost produktu

[!include [banner](../includes/banner.md)]

Kontroly připravenosti můžete použít pro to, aby vám pomohli zajistit, že pro produkt budou dokončena všechna požadovaná hlavní data před použitím v transakcích. Pokud se použijí kontroly připravenosti, je uživatel nebo tým odpovědný za ověření konkrétních předdefinovaných dat souvisejících s produktem.

Zaškrtávací políčko **Aktivní** pro technický produkt, variantu nebo verzi můžete zapnout až po zadání a ověření všech požadovaných dat a po zpracování všech kontrol připravenosti. Pokud pro produkt, verzi nebo variantu nebyla provedena jedna nebo více kontrol, pak se při pokusu o zapnutí políčka **Aktivní** zobrazí výzva s upozorněním, že nebyly dokončeny všechny kontroly.

Můžete vytvořit kontroly připravenosti pro nové technické produkty, varianty a verze. Kontroly připravenosti můžete také použít na standardní (netechnické) produkty (viz také [Kontroly připravenosti standardních produktů](#standard-products)). 

Standardní produkty můžete použít v transakcích, i když nebyly dokončeny všechny kontroly připravenosti. Pokud potřebujete zablokovat používání produktu v transakcích, použijte jeho stav životního cyklu. Můžete přiřadit stav životního cyklu, který blokuje používání produktu v transakcích, a následně po dokončení všech kontrol připravenosti přiřadit nový stav životního cyklu, který umožňuje požadované transakce.

## <a name="types-of-readiness-checks"></a>Typy kontrol připravenosti

Existují tři typy kontrol připravenosti:

- **Kontrola systému** - Systém ověří, zda existuje platný záznam. Například záznam může být aktivní kusovník (BOM).
- **Ruční kontrola** - Uživatel ověří, zda je záznam platný. Například kontrola připravenosti může vyžadovat ověření výchozího nastavení objednávky. V některých případech, například když se produkt stále navrhuje, a proto nebude umístěn na skladě, není nutné žádné výchozí nastavení objednávky. Výchozí nastavení objednávky však může být vyžadováno pro jiný produkt stejného typu, protože produkt lze držet na skladě. Uživatel je odpovědný za to, jak správně rozhodnout, když je vyžadována kontrola připravenosti.
- **Kontrolní seznam** - Uživatel odpovídá na řadu otázek z kontrolního seznamu a systém určuje, zda odpovědi splňují očekávání. Kontrolní seznam může mít jakýkoli předmět. Lze jej například použít k určení, zda jsou dokončeny marketingové materiály nebo dokumentace k produktu.

<a name="checks-engineering"></a>

## <a name="how-readiness-checks-are-created-for-a-new-engineering-product-variant-or-version"></a>Jak se vytvářejí kontroly připravenosti pro nový technický produkt, variantu nebo verzi

Zásady kontroly připravenosti lze použít na úrovni uvolněného produktu, úrovni uvolněné varianty a na úrovni technické verze.

Když vytvoříte nový *technický produkt*, systém určí, zda se na něho [platí zásady kontroly připravenosti](#assign-policy). Pokud se použijí zásady kontroly připravenosti, dojde k následujícím událostem:

- Pro produkt se podle příslušných zásad vytvářejí kontroly připravenosti.
- Technická verze je nastavena na neaktivní, aby zablokovala používání produktu. Všechny technické verze produktu jsou nastaveny na neaktivní.

Pokud je vytvořena *varianta* pro produkt, systém zkontroluje, zda se na něj vztahují zásady kontroly připravenosti. (Kontroly připravenosti lze použít na úrovni uvolněné varianty a na úrovni technické verze.) Pokud se vztahují zásady, dojde k následujícím událostem:

- Pro produkt se podle příslušných zásad vytvářejí kontroly připravenosti.
- Technická verze a varianta je nastavena na neaktivní, aby zablokovala používání produktu.

Pokud je vytvořena nová technická *verze* pro produkt, systém zkontroluje, zda se na něj vztahují zásady kontroly připravenosti. (Kontroly připravenosti lze použít na úrovni technické verze.) Pokud se vztahují zásady, dojde k následujícím událostem:

- Pro produkt se podle příslušných zásad vytvářejí kontroly připravenosti.
- Technická verze je nastavena na neaktivní, aby zablokovala používání produktu.

> [!NOTE]
> Můžete také nastavit zásady kontroly připravenosti na standardní (netechnické) produkty. Další informace viz [Kontroly připravenosti standardních produktů](#standard-products) dále v tomto tématu.

## <a name="view-readiness-checks"></a>Zobrazení kontrol připravenosti

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Zobrazení otevřených kontrol připravenosti produktu nebo verze produktu

Chcete-li vyhledat otevřené kontroly připravenosti produktu, otevřete stránku **Podrobnosti o uvolněných produktech**. Poté v podokně akcí na kartě **Produkt** ve skupině **Kontroly připravenosti** zvolte **Kontroly připravenosti**.

Chcete-li vyhledat otevřené kontroly připravenosti pro verzi produktu, otevřete stránku **Technické verze** pro uvolněný produkt a vyberte verzi. Poté v podokně akcí na kartě **Produkt** ve skupině **Kontrolní seznam** zvolte **Kontroly připravenosti**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Zobrazení otevřených kontrol připravenosti, které jsou vám přiřazeny

Chcete-li zobrazit otevřené kontroly připravenosti, které jsou vám přiřazeny, postupujte podle jednoho z těchto kroků.

- Přejděte na **Správa technických změn \> Společný \> Připravenost produktu \> Moje otevřené kontroly připravenosti**.
- Přejděte na **Správa informací o produktu \> Pracovní prostory \> Připravenost produktu pro diskrétní výrobu**.

Nastavení, které určuje, komu je přiřazena kontrola připravenosti, se provádí pro zásady připravenosti. Kontroly připravenosti lze přiřadit osobě nebo týmu. Pokud je kontrola připravenosti přiřazena týmu, je v týmu jedna osoba, která musí kontrolu připravenosti zpracovat.

## <a name="process-open-readiness-checks"></a>Zpracování otevřených kontrol připravenosti

### <a name="process-system-and-manual-readiness-checks"></a>Zpracování systémových a ručních kontrol připravenosti

Po otevření stránky **Kontroly připravenosti** můžete zobrazit předmět systémových a manuálních kontrol připravenosti výběrem možnosti **Zobrazit související informace** v podokně akcí. Poté můžete dokončit anebo ověřit data pro kontrolu připravenosti. Otevřené kontroly připravenosti mají hodnotu **Stavu** jako *Čekající*. Tento stav označuje, že kontrola připravenosti musí být stále zpracována. Chcete-li zpracovat kontrolu připravenosti, proveďte jeden z následujících kroků.

- V podokně akcí vyberte **Zkontrolovat/dokončit** pro zkontrolování a dokončení kontroly připravenosti. Po dokončení se pole **Stav** aktualizuje na *Úspěch*.
- V podokně akcí vyberte **Přeskočit**, pokud chcete přeskočit kontrolu připravenosti, která není povinná. Například nastavíte kontrolu připravenosti pro cenové výpočty. Rozhodnete se však tuto kontrolu přeskočit, když je produkt stále ve fázi návrhu. V tomto případě se pole **Stav** aktualizuje na *Přeskočeno*.

V závislosti na konfiguraci zásad připravenosti, když je pole **Stav** pro kontrolu připravenosti aktualizováno na *Úspěch*, může být vyžadován další krok ke schválení kontroly připravenosti. V takovém případě vyberte **Schválení** k dokončení kontroly připravenosti. Tento krok schválení je vždy povinný, když je kontrola připravenosti přeskočena.

Když byly všechny otevřené kontroly připravenosti nového produktu, varianty nebo verze zpracovány a schváleny podle potřeby, položka se automaticky aktivuje a je tedy připravena k použití.

### <a name="process-checklist-readiness-checks"></a>Zpracování kontrol připravenosti kontrolního seznamu

Chcete-li otevřít kontrolní seznam, otevřete stránku **Kontroly připravenosti** a poté na panelu akcí vyberte **Spustit kontrolní seznam**. Po dokončení kontrolního seznamu systém na základě nastavení v dotazníku ověří, zda je kontrola připravenosti úspěšná. Pokud je kontrola úspěšná, pole **Stav** je aktualizováno na *Úspěch*. Pokud kontrola připravenosti není povinná, můžete ji přeskočit. V tomto případě se pole **Stav** aktualizuje na *Přeskočeno*.

V závislosti na konfiguraci zásad připravenosti, když je pole **Stav** pro kontrolu připravenosti aktualizováno na *Úspěch*, může být vyžadován další krok ke schválení kontroly připravenosti. V takovém případě vyberte **Schválení** k dokončení kontroly připravenosti. Tento krok schválení je vždy povinný, když je kontrola připravenosti přeskočena.

Když byly všechny otevřené kontroly připravenosti nového produktu, varianty nebo verze zpracovány a schváleny podle potřeby, položka se automaticky aktivuje a je tedy připravena k použití.

## <a name="create-and-manage-product-readiness-policies"></a>Vytváření a správa zásad připravenosti produktu

Pomocí zásad připravenosti produktu můžete spravovat kontroly připravenosti, které se na produkt vztahují. Každá zásada připravenosti obsahuje sadu kontrol připravenosti. Když je zásadě připravenosti přiřazena kategorie technického produktu nebo sdílený pridukt, všechny produkty, které se vztahují k dané kategorii nebo sdílenému produktu budou mít kontroly připravenosti, které jsou uvedeny v zásadě připravenosti.

Chcete-li pracovat se zásadami připravenosti produktu, přejděte na **Správa technických změn \> Nastavení \> Zásady připravenosti produktu**. Potom proveďte jeden z následujících kroků.

- Chcete-li vytvořit novou zásadu, vyberte **Nová** v podokně akcí a poté nastavte pole, jak je popsáno v následujících podsekcích.
- Chcete-li upravit existující zásadu, vyberte ji v podokně seznamu, zvolte **Upravit** v podokně akcí a poté nastavte pole, jak je popsáno v následujících podsekcích.
- Chcete-li odstranit existující zásadu, vyberte ji v podokně seznamu a vyberte **Upravit** v podokně akcí a poté se na záložce s náhledem **Obecné** ujistěte, že možnost **Aktivní** je nastavena na *Ne*. Poté v podokně akcí zvolte **Odstranit**.

### <a name="header"></a>Záhlaví

V záhlaví zásad připravenosti produktu nastavte následující pole.

| Pole | popis |
|---|---|
| Jméno | Zadejte název zásady. |
| popis | Zadejte popis zásady. |

### <a name="general-fasttab"></a>Záložka s náhledem Obecné

Na záložce s náhledem **Obecné** zásad připravenosti produktu nastavte následující pole.

| Pole | popis |
|---|---|
| Typ produktu | Vyberte, zda se zásada vztahuje na produkty typu *Položka* nebo *Služba*. Po uložení záznamu toto nastavení nemůžete změnit. |
| Aktivní | Pomocí této možnosti můžete zachovat zásady připravenosti. Nastavte možnost na *Ano* pro všechny zásady připravenosti, které používáte. Nastavte ji na *Ne*, čímž označíte zásadu připravenosti jako neaktivní, když se nepoužívá. Všimněte si, že nemůžete deaktivovat zásadu připravenosti, která je přiřazena kategorii technického produktu nebo sdílenému produktu, a můžete odstranit pouze neaktivní zásady uvolnění. |

### <a name="readiness-control-fasttab"></a>Záložka s náhledem Kontrola připravenosti

Pro každý typ kontroly připravenosti, který chcete zahrnout do zásady, přidejte řádek na záložce s náhledem **Kontrola připravenosti**. Pomocí následujících tlačítek na panelu nástrojů záložky s náhledem můžete podle potřeby přidávat a odebírat řádky:

- **Přidat kontrolu** - Přidejte do zásady standardní kontrolu připravenosti. Když vyberete toto tlačítko, zobrazí se dialogové okno **Přidat kontrolu**. Zde si můžete vybrat ze seznamu dostupných kontrol.
- **Přidat stávající dotazník** - Přidejte do mřížky prázdný řádek. Poté můžete přiřadit existující dotazník nastavením polí v následující tabulce.
- **Kopírovat** - Přidejte kopii vybraného řádku do mřížky.
- **Odstranit** - Odstraňte vybraný řádek z mřížky.

Pro každý řádek, který přidáte, nastavte následující pole.

| Pole | popis |
| --- | --- |
| Oblast procesu | Vyberte oblast, které se kontrola týká. |
| Typ | Vyberte, zda jde o systémovou kontrolu, ruční kontrolu nebo kontrolní seznam (dotazník). |
| Jméno | Pokud jde o kontrolní seznam, zadejte název. U systémových a manuálních kontrol je toto pole nastaveno automaticky. |
| popis | Pokud jde o kontrolní seznam, zadejte popis. U systémových a manuálních kontrol je toto pole nastaveno automaticky a popis vysvětluje zaměření kontroly. |
| Použití kontrol | Vyberte, zda má řádek generovat kontroly připravenosti v reakci na nový uvolněný produkt, uvolněnou variantu nebo uvolněnou verzi. |
| Spustit v | Vyberte, zda se kontroly připravenosti, které řádek generuje, vztahují na všechny společnosti nebo na jednu společnost. |
| Společnost | Pokud nastavíte pole **Provést v** na *Jedna společnost*, vyberte společnost. |
| Typ vlastníka | Vyberte, zda kontroly připravenosti, které řádek generuje, by měly být přiřazeny osobě nebo týmu. |
| Vlastník | Vyberte osobu nebo tým, kterým mají být přiřazeny kontroly připravenosti generované řádkem. |
| Dotazník | Vyberte dotazník, který se má použít pro kontrolní seznam. Kontrolní seznam je místní kontrolní seznam ve společnosti, kde se provádí kontrola připravenosti. Systém musí být schopen vyhodnotit, zda je kontrolní seznam správně zodpovězen. Proto musí být kontrolní seznam nastaven tak, aby bylo hodnocení provedeno na základě správných odpovědí. Další informace o tom, jak vytvářet dotazníky, najdete v části [Použití dotazníků](/dynamicsax-2012/appuser-itpro/using-questionnaires) a souvisejících tématech. |
| Automatické schválení | Záznamy o kontrole připravenosti zahrnují zaškrtávací políčko **Schváleno** označující stav schválení. Vyberte zaškrtávací políčko **Automatické schválení** pro kontroly, které by měly být nastaveny na schválené ihned poté, co je přidělený uživatel dokončí. Zrušte zaškrtnutí tohoto políčka, chcete-li jako další krok vyžadovat výslovné schválení. |
| Povinné | Toto políčko zaškrtněte u kontrol, které musí přiřazený uživatel dokončit. Povinné kontroly nelze přeskočit. |

<a name="assign-policy"></a>

## <a name="assign-readiness-policies-to-standard-and-engineering-products"></a>Přiřaďte zásady připravenosti standardním a strojírenským produktům

Když vytvoříte nový produkt na základě technické kategorie, vytvoříte obojí *uvolněný produkt* a související *sdílený produkt*. Způsob vyřešení zásad připravenosti pro vydaný produkt závisí na tom, zda jste zapnuli funkci *Kontroly připravenosti produktu*. (Další informace viz [Kontroly připravenosti standardních produktů](#standard-products) dále v tomto tématu.)

- Když je funkce *Kontroly připravenosti produktu* *vypnuta* ve vašem systému, je zásada připravenosti nastavena a zobrazena pouze v záznamu [technické kategorie](engineering-versions-product-category.md). Chcete-li zjistit, jaké zásady platí pro vydaný produkt, systém zkontroluje pole **Zásady připravenosti produktu** pro související technickou kategorii. Zásadu připravenosti pro existující produkt můžete změnit úpravou související technické kategorie (nikoli sdíleného produktu).
- Když je funkce *Kontroly připravenosti produktu* *zapnuta*, přidá pole **Zásady připravenosti produktu** na stránku **Produkt** (kde jsou nastaveny sdílené produkty) a na stránku **Uvolněný produkt** (kde je hodnota jen pro čtení a je převzata ze souvisejícího sdíleného produktu). Systém najde zásadu připravenosti na vydaný produkt kontrolou souvisejícího sdíleného produktu. Když k vytvoření nového technického produktu použijete technickou kategorii, systém vytvoří sdílený produkt i uvolněný produkt a zkopíruje libovolné nastavení **Zásady připravenosti produktu** pro technickou kategorii do nového sdíleného produktu. Zásadu připravenosti pro existující produkt můžete potom změnit úpravou souvisejícího sdíleného produktu (nikoli uvolněné technické kategorie).

Pokud chcete ke sdílenému produktu přiřadit zásady připravenosti, postupujte takto.

1. Přejděte na **Informace o produktech \> Produkty \> Produkty**.
1. Otevřete nebo vytvořte produkt, kterému chcete přiřadit zásadu připravenosti.
1. Na pevné záložce **Obecné** nastavte pole **Zásady připravenosti produktu** na název zásady, která by se měla vztahovat na produkt.

Pokud chcete k technické kategorii přiřadit zásady připravenosti, postupujte takto.

1. Jděte na **Správa technických změn \> Nastavení \> Podrobnosti kategorie technického produktu**.
1. Otevřete nebo vytvořte technickou kategorii, kterému chcete přiřadit zásadu připravenosti.
1. Na pevné záložce **Zásady připravenosti produktu** nastavte pole **Zásady připravenosti produktu** na název zásady, která by se měla vztahovat na technickou kategorii.

<a name="standard-products"></a>

## <a name="readiness-checks-on-standard-products"></a>Kontroly připravenosti standardních produktů

Můžete povolit kontroly připravenosti produktu pro standardní (jiné než technické) produkty zapnutím funkce *Kontroly připravenosti produktu* ve Správě funkcí. Tato funkce provádí několik malých změn v systému kontroly připravenosti, aby podporovala standardní produkty.

### <a name="enable-readiness-checks-on-standard-products"></a>Povolit kontroly připravenosti standardních produktů

Chcete-li systému umožnit provádět kontroly připravenosti standardních produktů, postupujte takto.

- Povolte správu technických změn ve vašem systému, jak je popsáno v [Přehledu správy technických změn](product-engineering-overview.md).
- Použijte [Správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) k zapnutí funkce, která je pojmenována *Kontroly připravenosti produktu*.

<!-- KFM: This section requires confirmation before publishing

### How readiness checks are created for standard products

When you create a new non-engineering *released product*, the system determines whether a readiness check policy has been set up for the related shared product. If a policy has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

If a new *variant* is created for a product, the system checks whether readiness checks have been set up on the related shared product. If a readiness check has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

For engineering products, readiness checks are created in the same way that they are created when the *Product readiness checks* feature is turned off. For more information, see the [How readiness checks are created for a new engineering product, variant, or version](#checks-engineering) section earlier in this topic.

-->

### <a name="create-readiness-policies-for-standard-products"></a>Vytvořte zásady připravenosti pro standardní produkty

Zásady připravenosti pro standardní produkty vytváříte stejně jako pro technické produkty. Viz dřívější informace v tomto tématu.

### <a name="assign-readiness-policies-to-standard-products"></a>Přiřaďte zásady připravenosti pro standardní produkty

Chcete-li přiřadit zásadu připravenosti ke standardnímu produktu, otevřete související sdílený produkt a nastavte pole **Zásady připravenosti produktu** na název zásady, která by měla platit. Další informace viz sekce [Přiřaďte zásady připravenosti standardním a technickým produktům](#assign-policy) dříve v tomto tématu.

### <a name="view-and-process-readiness-checks-on-standard-products"></a>Zobrazit a zpracovat kontroly připravenosti standardních produktů

Když je tato funkce zapnutá, prohlížíte a zpracováváte kontroly připravenosti standardních produktů stejně jako u technických produktů. Viz dřívější informace v tomto tématu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
