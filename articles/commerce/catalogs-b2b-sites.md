---
title: Vytváření obchodních katalogů pro B2B weby
description: Toto téma popisuje, jak vytvořit katalogy Commerce pro weby elektronického obchodování typu business-to-business (B2B) v Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 868f6bbeefeb1698bb136d52c09cebf293c95731
ms.sourcegitcommit: 0abc777986112ea2332f5bf0e815b303b952356c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/29/2022
ms.locfileid: "8656832"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>Vytváření obchodních katalogů pro B2B weby

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Toto téma popisuje, jak vytvořit katalogy produktů Commerce pro weby elektronického obchodování typu business-to-business (B2B) v Microsoft Dynamics 365 Commerce. Odpovědi na často kladené otázky o katalozích Commerce pro B2B weby najdete v článku [Nejčastější dotazy k obchodním katalogům pro B2B](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> Toto téma se týká Microsoft Dynamics 365 Commerce verze 10.0.26 a novějších vydání.

Pomocí katalogů Commerce můžete identifikovat produkty, které chcete nabídnout na vašich internetových obchodech B2B. Když vytváříte katalog, identifikujete online obchody, ve kterých jsou produkty nabízeny, přidáte produkty, které chcete zahrnout, a rozšíříte nabídku produktů přidáním podrobností o merchandisingu. Pro každý B2B online obchod můžete vytvořit více katalogů.

Katalogy produktů Commerce vám umožňují definovat následující informace:

- **Hierarchie navigace specifická pro katalog** – Organizace mohou vytvořit odlišnou strukturu kategorií pro svůj konkrétní katalog.
- **Metadata atributů specifická pro katalog** – Atributy obsahují podrobnosti o produktu. Přiřazením atributů ke kategorii navigační hierarchie můžete definovat hodnoty pro tyto atributy na úrovni produktů, které jsou přiřazeny k dané kategorii. Organizace pak mohou provádět tyto úlohy:

    - Definovat hodnoty atributů produktu specifické pro katalog.
    - Řídit viditelnost atributů na úrovni katalogu.
    - Vybrat zpřesnění specifická pro jednotlivý katalog.

- **Kanály** – Organizace mohou ke katalogu přidružit více než jeden online kanál B2B. Úplná podpora pro katalogy je v současnosti dostupná pouze u internetových obchodů B2B.
- **Hierarchie zákazníků** – Pro daný B2B kanál mohou organizace zpřístupnit konkrétní katalog vybraným B2B partnerům tím, že k tomuto katalogu přiřadí zákaznické hierarchie.
- **Cenové skupiny** – Můžete nakonfigurovat ceny a akce, které jsou specifické pro daný katalog. Tato schopnost je hlavním důvodem pro definování katalogu pro B2B kanál. Cenové skupiny pro katalogy umožňují organizacím zpřístupnit produkty jejich zamýšleným B2B organizacím a uplatnit preferované ceny a slevy. B2B zákazníci, kteří si objednají zboží z konfigurovaného katalogu, mohou těžit ze speciálních cen a akcí poté, co se přihlásí na web Commerce B2B. Abyste mohli konfigurovat katalogové ceny, vyberte možnost **Cenové skupiny** na kartě **Katalogy** a propojte nejméně jednu cenovou skupinu s katalogem. Všechny obchodní smlouvy, deníky úprav cen a rozšířené slevy, které byly propojeny se stejnou cenovou skupinou, budou použity, když si zákazníci objednají z tohoto katalogu. (Pokročilé slevy zahrnují prahové, množstevní a kombinační slevy.) Další informace o cenových skupinách viz [Cenové skupiny](price-management.md#price-groups).

> [!NOTE]
> Tato funkce je k dispozici v aplikaci Dynamics 365 Commerce od verze 10.0.26. Chcete-li nastavit konfigurace specifické pro katalog, jako je hierarchie navigace a hierarchie zákazníků, otevřete v centrále Commerce pracovní prostor **Správa funkcí** (**Správa systému \> Pracovní prostory \> Správa funkcí**), zapněte funkci **Povolit použití více katalogů na maloobchodních kanálech** a poté spusťte úlohu **1110 CDX**.

## <a name="catalog-process-flow"></a>Tok procesu katalogu

Proces tvorby a zpracování katalogu má čtyři obecné kroky. Každý krok je podrobně vysvětlen v další části.

1. **[Konfigurace](#configure-the-catalog)**

    - Přiřaďte hierarchii navigace.
    - Uveďte data platnosti a data vypršení platnosti, pokud jsou relevantní.
    - Přidejte a kategorizujte produkty.
    - Přiřaďte cenové skupiny.
    - Přiřaďte zákaznickou hierarchii, která je specifická pro vaše B2B organizace. 
    - Přiřaďte výchozí skupinu atributů dimenze pro zpřesnění, jako je velikost, styl a barva.
    - Nastavte metadata atributů.

1. **[Ověření](#validate-the-catalog)** – V tomto kroku spustíte ověřovací pravidla, která vynucují specifické chování. Několik příkladů:

    - Ujistěte se, že neexistují žádné nekategorizované produkty.
    - Zkontrolujte, zda jsou všechny položky, které jsou přiřazeny k jednotlivým kanálům, přidruženy také ke katalogu.

1. **[Schválení](#approve-the-catalog)**
1. **[Publikování](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>Nastavení katalogu

K nastavení katalogu použijte informace v této části.

### <a name="configure-the-catalog"></a>Konfigurace katalogu

V centrále Commerce přejděte na **Maloobchod a obchod \> Katalogy a sortimenty \> Všechny katalogy** a konfigurujte katalog.

Když vytvoříte nový katalog, je nutné ho nejprve přiřadit k jednomu či více kanálům. Při vytváření katalogu lze použít pouze položky připojené k [sortimentu](/dynamics365/unified-operations/retail/assortments) vybraného kanálu. Chcete-li katalog přiřadit k jednomu nebo více kanálům, vyberte **Přidat** na záložce **Kanály Commerce** umístěné ve stránce **Nastavení katalogu**.

#### <a name="associate-the-navigation-hierarchy"></a>Přiřazení hierarchie navigace

Pokud chcete přidat produkty do katalogu, musíte vybrat hierarchii navigace. Hierarchie navigace podporuje strukturu kategorie pro katalog. Je třeba vybrat jednu z hierarchie navigace spojenou s maloobchodními kanály vybranými na pevné záložce **Kanály Commerce** stránky **Nastavení katalogu**. Chcete-li ke každému z vašich kanálů přiřadit výchozí hierarchii navigace, přejděte na **Maloobchod a obchod \> Nastavení kanálu \> Kategorie kanálů a atributy produktů**.

#### <a name="specify-time-effective-and-expiration-dates"></a>Zadání dat platnosti a dat vypršení platnosti

Chcete-li pro katalog zadat data platnosti a data vypršení platnosti, vyberte nejvyšší uzel hierarchie katalogu a vraťte se do zobrazení záhlaví hlavního katalogu. Poté na pevné záložce **Obecné** podle potřeby konfigurujte datum platnosti a datum vypršení podle potřeby .

#### <a name="add-and-categorize-products"></a>Přidání a kategorizace produktů

Chcete-li konfigurovat produkty k přidání do katalogu, přejděte v centrále Commerce na **Maloobchod a obchod \> Katalogy a sortimenty \> Všechny katalogy**. Poté na kartě **Katalogy** vyberte **Přidat produkty**.

Případně vyberte uzel v hierarchii navigace. Poté budete moci přidávat produkty přímo do kategorie v katalogu.

#### <a name="associate-price-groups"></a>Přiřazení cenových skupin

Chcete-li konfigurovat ceny specifické pro katalog, musíte s katalogem propojit jednu nebo více cenových skupin. Chcete-li propojit cenové skupiny s katalogem, přejděte v centrále Commerce na **Maloobchod a obchod \> Katalogy a sortimenty \> Všechny katalogy**. Poté na kartě **Katalogy** v části **Cenová kalkulace** vyberte **Cenové skupiny**. Všechny obchodní smlouvy, deníky úprav cen a maloobchodní rozšířené slevy (prahová hodnota, množství, kombinace a shoda), které byly propojeny se stejnou cenovou skupinou, budou použity, když si zákazníci objednají z tohoto katalogu.

Další informace o cenových skupinách naleznete v tématu [Cenové skupiny](price-management.md#price-groups).

> [!NOTE]
> Novou cenovou skupinu nemůžete vytvořit na stránce **Všechny katalogy**. Místo toho ji musíte vytvořit na stránce **Všechny cenové skupiny**. Poté ji musíte přiřadit ke katalogu na stránce **Všechny katalogy**.

#### <a name="associate-a-customer-hierarchy"></a>Přidružení hierarchie zákazníků

Chcete-li přidružit hierarchie zákazníků, přejděte v centrále Commerce na **Maloobchod a obchod \> Katalogy a sortimenty \> Všechny katalogy**. Poté na kartě **Katalogy** v části **Hierarchie zákazníků** vyberte **Přiřadit hierarchie** a propojte jednu nebo více zákaznických hierarchií s katalogem.

> [!NOTE]
> Novou hierarchii zákazníků nemůžete vytvořit na stránce **Všechny katalogy**. Místo toho ji musíte vytvořit na stránce **Hierarchie zákazníků**. Poté ji musíte přiřadit ke katalogu na stránce **Všechny katalogy**.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>Přidružení výchozí skupiny atributů dimenze pro zpřesnění, jako je velikost, styl a barva

Chcete-li přidružit výchozí skupinu atributů dimenze ke zpřesnění, jako je velikost, styl a barva, přejděte v ústředí Commerce do nabídky **Maloobchod a obchod \> Katalogy a sortimenty \> Všechny katalogy**. Poté na kartě **Katalogy** v části **Atributy** vyberte **Skupiny atributů**.

#### <a name="set-attribute-metadata"></a>Nastavit metadata atributu

Chcete-li konfigurovat metadata atributů, přejděte v centrále Commerce na **Maloobchod a obchod \> Katalogy a sortimenty \> Všechny katalogy**. Poté na kartě **Katalogy** v části **Atributy** vyberte **Nastavit metadata atributů**. Chcete-li vybrat atributy, které by měly být viditelné a upřesnitelné, vyberte kategorii v přidružené hierarchii navigace specifické pro katalog a poté v části **Atributy produktu katalogu** vyberte atribut. Poté vyberte možnost **Zobrazit atribut na kanálu**. Ve výchozím nastavení lze všechny zobrazitelné atributy také vyhledávat. Chcete-li atributy volitelně upravit, zapněte možnost **Lze upřesnit**.

### <a name="validate-the-catalog"></a>Ověření katalogu

Nový katalog musí být ověřen a publikován předtím, než bude k dispozici pro používání.

Katalog ověříte takto.

1. Na kartě **Katalogy** ve stránce **Všechny katalogy** v části **Ověřit** vyberte možnost **Ověřit katalog** a spusťte ověření. Tento krok je povinný. Ověří, zda je požadované nastavení přesné.
1. Chcete-li zobrazit detaily ověření, vyberte možnost **Zobrazit výsledky**. Pokud budou nalezeny chyby, musíte opravit data a znovu spustit ověření, dokud nebude úspěšné.

### <a name="approve-the-catalog"></a>Schválit katalog

Po ověření katalogu je nutné ho schválit.

Pomocí následujících kroků zahajte pracovní postup schvalování katalogu.

1. V podokně akcí ve stránce **Všechny katalogy** vyberte **Pracovní postup \> Odeslat**.
1. Přejděte do nabídky **Maloobchod a obchod \> Nastavení centrály \> Workflow obchodu** a konfigurujte kroky a autorizované uživatele pro pracovní postup. Pracovní postup definuje kroky potřebné k přesunutí katalogu do stavu **Schváleno**.

### <a name="publish-the-catalog"></a>Publikování katalogu

Poté, co je katalog ve stavu **Schváleno**, můžete jej publikovat výběrem příkazu **Publikovat** v nabídce **Katalogy**. Jakmile je katalog ve stavu **publikován**, lze jej použít k zadávání objednávek call centra a procesy odeslání katalogu. Katalog můžete publikovat buď ručně, nebo pomocí dávkového procesu. Datum platnosti, které jste pro katalog definovali, určuje, odkdy budou produkty dostupné v online obchodě. Datum vypršení platnosti, které jste definovali, určuje, kdy budou produkty odstraněny z online obchodu.

> [!NOTE]
> Můžete publikovat katalog obsahující produkty, které mají varování. Tyto produkty se však v internetovém obchodě neobjeví.

## <a name="additional-resources"></a>Další prostředky

[Dopad rozšiřitelnosti u přizpůsobení funkce Katalogy Commerce pro B2B](catalogs-b2b-sites-dev.md)

[Nejčastější dotazy k obchodním katalogům pro B2B](catalogs-b2b-sites-FAQ.md)
