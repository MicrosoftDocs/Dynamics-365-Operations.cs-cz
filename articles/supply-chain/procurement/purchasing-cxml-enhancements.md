---
title: cXML rozšíření nákupu
description: Funkce cXML rozšíření nákupu vychází z existující funkce externího katalogu, PunchOut, která se používá pro nákupní žádanky.
author: dasani-madipalli
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatCXMLParameters, CatCXMLPurchRequest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-08-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: d61087d21035e532ad86b6669626f55e8411a6f421bf69f817199e9063417761
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779607"
---
# <a name="purchasing-cxml-enhancements"></a>cXML rozšíření nákupu

[!include [banner](../includes/banner.md)]

Funkce _cXML rozšíření nákupu_ vychází z [existující funkce externího katalogu](set-up-external-catalog-for-punchout.md), která se používá pro nákupní žádanky. Tato existující funkce je známá jako _PunchOut_. Přestože nákupní objednávka nemusí pocházet z nákupní žádanky, musí existovat spojení mezi dodavatelem na nákupní objednávce a parametry, které se používají k odeslání dokladu o nákupní objednávce.

## <a name="turn-on-the-purchasing-cxml-enhancements-feature"></a>Zapnout funkci cXML rozšíření nákupu

Funkci zapnete otevřením stránky **[správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** a vyhledáním funkce s názvem *cXML rozšíření nákupu*. Vyberte funkci a zapněte ji volbou **Povolit nyní**.

Po zapnutí této funkce byste měli nakonfigurovat nastavení v následujících třech oblastech:

- **[Parametry cXML](#cxml-parameters)** - Pomocí těchto nastavení můžete nastavit některé globální parametry pro funkci odesílání nákupních objednávek.
- **[Nastavení dodavatele](#vendor-setup)** - Pokud by měl být používán komerční jazyk cXML ve výchozím nastavení pro všechny nové nákupní objednávky, které jsou vytvořeny pro libovolného dodavatele, nastavte možnost **Odeslat nákupní objednávku pomocí cXML** na _Ano_ pro toho prodejce.
- **[Externí katalogy](#external-catalog-setup)** - Použijte nové nastavení **Vlastnosti objednávky** k definování formátu dokladu nákupní objednávky a způsobu odeslání.

Následující obrázek shrnuje tuto konfiguraci.

![Oblasti pro nastavení funkcí cXML.](media/cxml-settings-areas.png "Oblasti pro nastavení funkcí cXML")

Kromě toho musíte nastavit [dávkovou úlohu požadavku na nákupní objednávku](#po-batch). Tato dávková úloha se používá k odeslání potvrzených nákupních objednávek.

## <a name="set-up-global-cxml-parameters"></a><a name="cxml-parameters"></a>Nastavení globálních parametrů cXML

Použijte stránku **Parametry cXML** pro provedení několika globálních nastavení, která se použijí na funkci pro odesílání nákupních objednávek.

![Stránka parametrů cXML.](media/cxml-parameters.png "Stránka parametrů cXML")

Přejděte na **Zásobování a zdroje \> Nastavit \> Správa cXML \> Parametry cXML** a nastavte následující parametry:

- **Režim testování cXML** - Tento globální parametr ovlivňuje způsob, jakým jsou nákupní objednávky fyzicky odesílány z dávkové úlohy. Vyberte jednu z následujících hodnot:

    - **Test** - V tomto režimu může být spuštěna dávková úloha a vygeneruje se XML dokument pro zprávu, ale nebude odeslán. Místo toho je uložen v žádosti o nákupní objednávku pro účely kontroly. Tento režim je užitečný, když jste v počáteční implementaci a chcete vidět, jak se do zprávy cXML zadávají data. Můžete také chtít vygenerovat ukázkové zprávy, které můžete odeslat prodejcům k počátečnímu ověření.
    - **Ostré nasazení** - V tomto režimu funkce používá [nastavení externího katalogu](#external-catalog-setup) pro fyzické předání každého dokumentu dodavateli.

- **Odeslat aktualizace nákupní žádanky** - Nastavte tuto možnost na *Ano* k odeslání zprávy o aktualizaci pro nákupní objednávky. Nastavte ji na *Ne*, abyste zabránili odeslání zprávy. Většina dodavatelů upřednostňuje zprávy o aktualizaci nedostávat. Místo toho vyžadují, aby je zákazníci v případě změny nákupní objednávky kontaktovali telefonicky nebo e-mailem. Tento parametr je globální parametr a u každého dodavatele nelze v externím katalogu zadat žádné přepsání. Nákupní objednávka bude označena jako aktualizovaná, pokud na nákupní objednávce zaúčtujete druhé potvrzení, ale první potvrzení již bylo odesláno a potvrzeno prodejcem. Pokud existuje druhé potvrzení, ale první potvrzení nebylo odesláno, bude druhé potvrzení považováno za nový dokument. Dokud nebude odesláno jedno potvrzení, můžete nákupní objednávku potvrdit kolikrát chcete. Další potvrzení bude poté považováno za zprávu o aktualizaci.
- **Odeslat odstranění nákupní žádanky** - Nastavte tuto možnost na *Ano* k odstranění zprávy o aktualizaci pro nákupní objednávky. Nastavte ji na *Ne*, abyste zabránili odeslání zprávy. Většina dodavatelů upřednostňuje zprávy o odstranění nedostávat. Místo toho vyžadují, aby je zákazníci v případě odeslání nákupní objednávky omylem kontaktovali telefonicky nebo e-mailem. Tento parametr je globální parametr a u každého dodavatele nelze v externím katalogu zadat žádné přepsání. Nákupní objednávka bude označena jako odstraněná, pokud nákupní objednávku zrušíte v Supply Chain Management.
- **Archivovat soubor** - Určete cestu k souboru, kam chcete exportovat a uložit archivované dokumenty cXML. Cesta se použije, když spustíte funkci čištění ze stránky **Žádost o nákupní objednávku**.
- **Maximální počet znaků pro řádek ulice** - Zadejte maximální počet znaků, které lze použít v poli ulice pro adresy v dokumentu cXML. Tento globální parametr ovlivňuje všechny dodavatele, pokud není ve vlastnostech externího katalogu zadáno přepsání.

## <a name="set-up-vendor-purchase-orders-to-use-cxml"></a><a name="vendor-setup"></a>Nastavení nákupní objednávky dodavatele pro použití cXML

Pokaždé, když potvrdíte nákupní objednávku, kde je možnost **Odeslat nákupní objednávku pomocí cXML** nastavena na _Ano_, systém automaticky vygeneruje zprávu cXML a doručí ji dodavateli, který je přidružen k dané nákupní objednávce. Tuto možnost můžete u svých nákupních objednávek ovládat dvěma způsoby:

- Chcete-li nastavit dodavatele tak, aby automaticky používal cXML pro všechny nové nákupní objednávky, které jsou vytvořeny z žádanky, přejděte na **Zásobování a zdroje \> Dodavatelé \> Všichni dodavatelé** a vyberte nebo vytvořte dodavatele, abyste otevřeli stránku podrobností. Pak na záložce s náhledem **Výchozí hodnoty nákupní objednávky** nastavte možnost **Odeslat nákupní objednávku pomocí cXML** na _Ano_. Pokud by cXML mělo být automaticky použito i pro nové nákupní objednávky, které **nejsou** vytvořené z žádanky, musíte také nastavit vlastnost objednávky **ENABLEMANUALPO** na _True_ pro související externí katalog, jak je popsáno později v tomto tématu v části [Nastavení vlastností objednávky](#set-order-properties).
- Pro jednotlivé nákupní objednávky přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky** a výběrem nebo vytvořením nákupní objednávky otevřete stránku s podrobnostmi. Přepněte na zobrazení **Záhlaví** a poté na záložce s náhledem **Nastavení** nastavte možnost **Odeslat nákupní objednávku pomocí cXML** podle potřeby.

![Výchozí nastavení pro nákupní objednávky dodavatele.](media/cxml-order-defaults.png "Výchozí nastavení pro nákupní objednávky dodavatele")

## <a name="set-up-an-external-catalog-to-use-cxml"></a><a name="external-catalog-setup"></a>Nastavení externího katalogu pro použití cXML

Na stránce **Externí katalogy** pro každý z vašich katalogů můžete nastavit funkci PunchOut a funkci pro odesílání nákupních objednávek. Příslušná nastavení najdete na **Zásobování a zdroje \> Katalogy \> Externí katalogy**. Začněte [nastavení každého katalogu jako obvykle](set-up-external-catalog-for-punchout.md). Tento proces zahrnuje přiřazení dodavatele, výběr kategorií, které má dodavatel povoleno dodávat, a aktivaci katalogu. Poté nakonfigurujte další nastavení, která jsou popsána v této části.

> [!NOTE]
> Když potvrdíte nákupní objednávku, kterou lze odeslat prostřednictvím cXML, systém vyhledá dodavatele, který je přidružen k nákupní objednávce, a poté najde první aktivní externí katalog, který je přidružen k danému dodavateli. Systém poté použije nastavení z tohoto externího katalogu k odeslání nákupní objednávky. Pokud je nastaveno více externích katalogů, systém použije pouze první externí katalog, který najde, na základě dodavatele v nákupní objednávce. Proto doporučujeme, abyste pro každého dodavatele vytvořili pouze jeden externí katalog.

![Nastavení externího katalogu.](media/cxml-supplier-catalog.png "Nastavení externího katalogu")

### <a name="set-the-punchout-protocol-type"></a>Nastavení typu protokolu PunchOut

Na záložce s náhledem **Obecné** stránky **Externí katalogy** nastavte pole **Typ protokolu Punchout** na _cXML_. Tato možnost bude jedinou dostupnou možností, pokud partner nerozšíří funkčnost a neposkytne v rozšíření další možnost.

Pokud také používáte katalog pro PunchOut, musíte také [nastavit formát zprávy](set-up-external-catalog-for-punchout.md). Formát zprávy se používá k navázání připojení k prodejci v transakci PunchOut z žádanky. Po odeslání nákupní objednávky se vlastnosti objednávky použijí k navázání spojení s dodavatelem.

### <a name="set-the-order-properties"></a><a name="set-order-properties"></a>Nastavení vlastností objednávky

Funkce _cXML rozšíření nákupu_ přidává novou záložku s náhledem **Vlastnosti objednávky** pro externí katalogy. Tato záložka s náhledem poskytuje mřížku, kde můžete definovat vlastnosti objednávky. Poskytuje také panel nástrojů. Tento panel nástrojů obsahuje následující tři tlačítka, která můžete použít ke správě vlastností objednávky:

- **Výchozí vlastnosti** - Když nastavujete nový katalog, vyberte toto tlačítko a přidejte do mřížky předdefinovanou kolekci běžně používaných vlastností.
- **Nová** - Přidejte novou vlastnost do mřížky.
- **Odstranit** - Odstranit aktuálně vybranou vlastnost z mřížky. Pokud omylem odstraníte výchozí vlastnost, vyberte **Výchozí vlastnosti** a obnovte všechny chybějící vlastnosti.

Pokaždé, když do mřížky přidáte jednu nebo více vlastností, použijte pravý sloupec pro určení hodnot každé z nich.

Výchozí vlastnosti použijte následujícím způsobem:

- **BUYER\_COOKIE** - Toto sledovací pole lze použít k označení konkrétních informací pro vaši společnost. Pokud nemáte s dodavatelem dohodu o tom, jak se tato vlastnost používá, nemá při odesílání nákupní objednávky příliš velký význam. Proto byste ji měli nastavit na jednoduchou hodnotu.
- **DELIVERTO** - Když je v dokladu z nákupní objednávky uvedena dodací adresa, pole **Informace o upozornění** se používá k nastavení pole **DeliverTo** ve zprávě XML. Pokud požadujete, aby tato hodnota byla jménem žadatele, a nastavíte pole žadatele v záhlaví nákupní objednávky, zadejte hodnotu _REQUESTER_ pro tuto vlastnost, takže jméno žadatele bude zadáno v poli **DeliverTo** v XML. V tomto případě bude použitá primární e-mailová adresa a telefonní číslo od žadatele místo od objednatele.
- **DEPLOYMENTMODE** - Nastavte tuto vlastnost podle požadavků dodavatele. Hodnoty jsou obvykle _PRODUCTION_ nebo _TEST_. Nastavte hodnotu na základě vaší komunikace s dodavatelem. Obvykle musí odpovídat zamýšlenému systému za hodnotou **ORDERCHECKURL**, kterou dodavatel označuje jako testovací nebo produkční systém.
- **FIXEDBILLADDRESSID** - Když je nastaveno pole **addressID** ve zprávě XML, vybere místo, které je uvedeno na adrese. Pokud se hodnota ID, kterou jste sdělili dodavateli, z nějakého důvodu liší od hodnoty na místě adresy, můžete vynutit přepsání zadáním hodnoty zde. Předpokládá se, že u dodavatele použijete pouze jednu adresu a že adresa je nastavena v systému dodavatele. Fakturační adresa je primární fakturační adresa, která je uvedena pro právnickou osobu v aplikaci Supply Chain Management.
- **FIXEDSHIPADDRESSID** - Když je nastaveno pole **addressID** ve zprávě XML, vybere místo, které je uvedeno na adrese. Pokud se hodnota ID, kterou jste sdělili dodavateli, z nějakého důvodu liší od hodnoty na místě adresy, můžete vynutit přepsání zadáním hodnoty zde. Předpokládá se, že u dodavatele použijete pouze jednu adresu a že adresa je nastavena v systému dodavatele. Dodací adresa je adresa uvedená v záhlaví nákupní objednávky. Většina dodavatelů akceptuje pouze adresy záhlaví, nikoli adresy řádku. Ačkoli v XML existují pole pro adresy řádku, budou nastavena na adresu záhlaví.
- **FROM\_DOMAIN** - Zadejte hodnotu, která se použije k odeslání dokladů nákupní objednávky. Tuto hodnotu poskytuje váš dodavatel.
- **FROM\_IDENTITY** - Zadejte hodnotu, která se použije k odeslání dokladů nákupní objednávky. Tuto hodnotu poskytuje váš dodavatel.
- **ORDERCHECKURL** - Zadejte adresu URL, na kterou se mají odeslat dokumenty nákupní objednávky. Tato adresa URL začíná `https://` a poskytuje ji váš dodavatel.
- **PAYLOAD\_ID** - Zadejte hodnotu předpony pro ID datové části, jak je požadováno pro obchodní procesy, které jsou k dispozici pro aktuálního dodavatele.
- **SENDER\_DOMAIN** - Zadejte hodnotu, která se použije k odeslání dokladů nákupní objednávky. Tuto hodnotu poskytuje váš dodavatel.
- **SENDER\_IDENTITY** - Zadejte hodnotu, která se použije k odeslání dokladů nákupní objednávky. Tuto hodnotu poskytuje váš dodavatel.
- **SHARED\_SECRET** - Zadejte hodnotu, která se použije k odeslání dokladů nákupní objednávky. Tuto hodnotu poskytuje váš dodavatel.
- **STREETLENGTH** - Zadejte číslo, které představuje maximální počet znaků, které dodavatel přijme jako název ulice. Pokud je zde zadána hodnota, přepíše hodnotu zadanou na stránce **parametry cXML**. Systém odebere zalomení řádků a mezery, aby se pokusil přizpůsobit standardní adresu v aplikaci Supply Chain Management na počet znaků, který je zde uveden. Jakékoli další znaky budou zkráceny.
- **TO\_DOMAIN** - Zadejte hodnotu, která se použije k odeslání dokladů nákupní objednávky. Tuto hodnotu poskytuje váš dodavatel.
- **TO\_IDENTITY** - Zadejte hodnotu, která se použije k odeslání dokladů nákupní objednávky. Tuto hodnotu poskytuje váš dodavatel.
- **USERAGENT** - Zadejte hodnotu k identifikaci systému, který používáte. Zadejte například _Dynamics 365 Supply Chain Management_.
- **VERSION** - Zadejte číslo verze cXML, pokud dodavatel požaduje tyto informace. Výchozí verze je *1.2.008*. Tato verze je stabilní a většina dodavatelů ji přijímá.
- **RESPONSETEXT** - Do zprávy odpovědi cXML po odeslání objednávky zadejte jakýkoli vlastní text, který očekáváte od dodavatele. Tímto způsobem může systém označit zprávu jako _Potvrzenou_. Pokud odpověď neodpovídá standardnímu textu nebo textu zákazníka, který zde zadáte, bude požadavek označen jako _Chyba_.
- **RESPONSETEXTSUB** - Nastavte tuto vlastnost na _TRUE_, chcete-li hledat v textu odpovědi dodavatele hodnoty, které jsou uvedeny v poli **RESPONSETEXT**. Dodavatel může například vrátit dlouhý řetězec, který v odpovědi obsahuje „OK“. V tomto případě můžete zadat _OK_ v poli **RESPONSETEXT** a nastavit **RESPONSETESTSUB** na _TRUE_ pro vyhledání „OK“ kdekoli v odpovědi. Objednávku lze poté nastavit na _Potvrzeno_.
- **CONTENTTYPE** - V typickém nastavení katalogu nemusíte tuto vlastnost nastavovat. Pokud se vám při odeslání nákupní objednávky zobrazí chyba serveru 500 ze systému dodavatele, můžete provést testování nastavením této vlastnosti na _FALSE_. Tato hodnota změní nastavení ve webovém požadavku a může umožnit odeslání zprávy pro některé platformy.
- **ENABLEHEADERS** - Nastavte tuto vlastnost na _TRUE_ pro odeslání záhlaví společně s objednávkou. Tuto vlastnost musíte nastavit, pouze pokud to vyžaduje dodavatel. Pokud nastavíte tuto vlastnost na _TRUE_, přidejte další vlastní vlastnosti, které jsou založeny na jménech, které prodejce poskytuje, a přidejte před ně předponu _H\__. Mezi typické příklady patří **H\_USERID**, **H\_PASSWORD**, **H\_RECEIVERID** a **H\_ACTIONREQUEST**. Následující vlastní vlastnosti jsou zahrnuty ve výchozích vlastnostech:

    - **H\_USERID** - Pokud obchodní partner požaduje, abyste jako součást adresy URL odeslali ID uživatele k odeslání nákupní objednávky, zadejte zde hodnotu.
    - **H\_PASSWORD** - Pokud obchodní partner požaduje, abyste jako součást adresy URL odeslali heslo k odeslání nákupní objednávky, zadejte zde hodnotu.

- **ENABLEMANUALPO** - Pokud je tato vlastnost nastavena na _TRUE_, když uživatelé ručně vytvářejí nákupní objednávky (tj. když nezačínají od žádanky), tyto nákupní objednávky zdědí nastavení z možnosti **Odeslat nákupní objednávku přes cXML** od dodavatele. Pokud tato vlastnost není nastavena nebo je nastavena na _FALSE_, možnost **Odeslat nákupní objednávku přes cXML** nebude nastavena v záhlaví nákupní objednávky pro ručně vytvořené nákupní objednávky. Pro nákupní objednávky, které jsou vytvořeny z žádanky, nastavení možnosti **Odeslat nákupní objednávku přes cXML** je vždy zděděno od dodavatele, bez ohledu na nastavení této vlastnosti. Další informace naleznete v části [Nastavení nákupní objednávky dodavatele pro použití cXML](#vendor-setup) dříve v tomto tématu.
- **PUNCHOUTPOONLY** - Pokud je tato vlastnost nastavena na _TRUE_, nastaví pouze řádky nákupní žádanky, které jsou vytvořeny z procesu PunchOut, možnost **Odeslat nákupní objednávku přes cXML** v záhlaví nákupní objednávky. Kromě toho musí být typ řádku nákupní žádanky u všech řádků na nákupní objednávce _Položka externího katalogu_. Jinak nelze vytvořit nákupní objednávku cXML.
- **PUNCHOUTSHIPTO** - Pokud je tato vlastnost nastavena na _TRUE_, výchozí adresa právnické osoby bude přidána do zprávy žádosti o nastavení PunchOut, když uživatel otevře externí katalog. Tato adresa je přidána jako adresa **ShipTo**. Dodavatelé budou používat adresu **ShipTo** pro zobrazení cen na základě místa společnosti.
- **TRACEPUNCHOUT** - Nastavte tuto vlastnost na _TRUE_, pokud se vám při pokusu o procházení externího katalogu z žádanky zobrazí chybová zpráva. Informace o sledování budou poté vyplněny pro zprávy **PunchOutSetupRequest** a **PunchOutResponse**, které jsou odesílány mezi Supply Chain Management a webem dodavatele. Tyto informace si můžete zobrazit na stránce **Protokol zpráv košíku cXML**, kterou můžete otevřít ze stránky **Nastavení externího katalogu** pro katalog dodavatelů, se kterými máte problémy. Tuto vlastnost byste měli nastavit na _TRUE_, pouze pokud odstraňujete problémy, protože to vytváří velkou zátěž pro výkon v databázi pro každý PunchOut. Další informace naleznete v části [Zobrazení protokolu zpráv košíku cXML pro externí katalog PunchOut](#message-log) dále v tomto tématu.
- **REPLACENEWLINE** - Nastavte tuto vlastnost na _TRUE_, pokud máte problém, protože systém dodavatele odesílá zprávu **PunchOutResponse**, která obsahuje znaky nového řádku (\\n). K tomuto problému může dojít, pokud jsou zprávy dodavatele analyzovány prostřednictvím middlewaru nebo centra zásobování. Pokud máte problém s nastavením nového dodavatele, nastavte vlastnost **TRACEPUNCHOUT** na _TRUE_ pro zobrazení zprávy **PunchOutResponse** a určení, zda jsou značky XML rozděleny znaky nového řádku.
- **POCOMMENTS** - Nastavte tuto vlastnost na _TRUE_, pokud chcete, aby dokument cXML obsahoval poznámky, které jsou připojeny k nákupní objednávce v Supply Chain Management. Text přílohy je obsažen v komentářích záhlaví ve zprávě nákupní objednávky. Další informace o tom, jak systém vybírá a zpracovává tyto přílohy, najdete v části [Připojení poznámek k nákupní objednávce](#attach-po-notes) dále v tomto tématu.
- **VENDCOMMENTS** - Nastavte tuto vlastnost na _TRUE_, pokud chcete, aby dokument cXML obsahoval poznámky, které jsou připojeny k nákupní objednávce v Supply Chain Management. Text přílohy je obsažen v komentářích záhlaví ve zprávě nákupní objednávky. Další informace o tom, jak systém vybírá a zpracovává tyto přílohy, najdete v části [Připojení poznámek k nákupní objednávce](#attach-po-notes).
- **CLEANAMP** - Nastavte tuto vlastnost na _TRUE_, pokud se zobrazí chybová zpráva, když se pokusíte provést PunchOut k dodavateli a zpáteční adresa URL dodavatele obsahuje nesprávně zakódované ampersandy (\&).
- **PUNCHOUTTZ** - Nastavte tuto vlastnost na _TRUE_, pokud prodejce, se kterým pracujete, používá ke specifickému ověřování data/času zprávy požadavku PunchOut normu ISO 8601. Supply Chain Management používá datum koordinovaného světového času (UTC) ve zprávě **PunchOutSetupRequest**. Proto když nastavíte tuto vlastnost na _TRUE_, je přidáno do formátu data/času *+00: 00*.
- **WMSADDRESSID** - Nastavte tuto vlastnost na _TRUE_ pro použití čísla skladu v záhlaví nákupní objednávky jako hodnoty **addressID** v adrese **ShipTo** pro požadavek na nákupní objednávku, který je odeslán dodavateli. Pokud nastavíte hodnotu pro vlastnost **FIXEDSHIPADDRESSID**, má tato hodnota přednost před touto hodnotou. Proto byste měli použít jednu nebo druhou vlastnost k nastavení hodnoty **addressID** v adrese **ShipTo** pro dokument.
- **PUNCHOUTSHIPTOUSER** - Tato vlastnost funguje společně s vlastností **PUNCHOUTSHIPTO**. Pokud je **PUNCHOUTSHIPTO** nastaveno na _TRUE_, je vybrána adresa právnické osoby. Pokud je **PUNCHOUTSHIPTOUSER** nastaveno na _TRUE_, místo adresy právnické osoby se použije primární adresa od uživatele PunchOut.

### <a name="activate-the-external-catalog"></a>Aktivace externího katalogu

Po dokončení nastavení všech vlastností a konfiguraci dalších nastavení externího katalogu přejděte zpět na záložku s náhledem **Obecné** ze stránky **Externí katalogy** a nastavte možnost **Aktivní** na *Ano*.

### <a name="attach-notes-to-a-purchase-order"></a><a name="attach-po-notes"></a>Připojení poznámek k nákupní objednávce

Jak bylo uvedeno v části [Nastavení vlastností objednávky](#set-order-properties), pokud chcete, aby vaše poskytnuté cXML obsahovalo text z poznámek připojených k příslušné nákupní objednávce nebo k záznamům dodavatele, můžete nastavit vlastnosti **POCOMMENTS** anebo **VENDCOMMENTS** na _TRUE_ v nastavení externího katalogu. Tato část poskytuje více podrobností o tom, jak systém vybírá a zpracovává tyto přílohy, pokud je používáte.

Chcete-li nastavit typy poznámek, které bude systém hledat, přejděte na **Zásobování a zdroje \> Nastavit \> Formuláře \> Z nastavení**. Pak na kartě **Nákupní objednávka** nastavte pole **Zahrnout dokumenty typu** na typ poznámky, kterou chcete zahrnout. Zahrnuty budou pouze textové poznámky, nikoli přílohy v podobě dokumentů.

![Stránka nastavení formuláře.](media/cxml-form-setup.png "Stránka nastavení formuláře")

Přílohy budou k nákupní objednávce zahrnuty, pouze pokud je pole **Typ** nastaveno na hodnotu, kterou vyberete v poli **Zahrnout dokumenty typu**, a pokud jejich pole **Omezení** je nastaveno na _Externí_. Chcete-li vytvořit, zobrazit nebo upravit přílohy nákupní objednávky, přejděte na **Zásobování a zdroje \> Všechny nákupní objednávky**, vyberte nebo vytvořte nákupní objednávku a poté vyberte tlačítko **Přílohy** (symbol kancelářské sponky) v pravém horním rohu.

![Přiložená poznámka, která je nastavena k odeslání dodavateli.](media/cxml-note-to-vendor.png "Přiložená poznámka, která je nastavena k odeslání dodavateli")

## <a name="view-the-cxml-cart-message-log-for-external-catalog-punchout"></a><a name="message-log"></a>Zobrazit protokol zpráv košíku cXML pro externí katalog PunchOut

Když nastavíte pole **Typ protokolu Punchout** na _cXML_ u externího katalogu, systém zaznamená protokol zpráv košíků, které přicházejí zpět od dodavatelů. Tento protokol lze použít pro řešení potíží a další datové účely.

Chcete-li otevřít protokol pro externí katalog, vyberte příslušný katalog a poté v podokně akcí vyberte **Protokol zpráv košíku cXML**. Stránka **Protokol zpráv košíku cXML** zobrazuje seznam košíků, které byly vráceny, XML související s těmito košíky a řádky, které byly vytvořeny v související nákupní žádance.

![Stránka protokolu zpráv košíku cXML.](media/cxml-cart-message-log.png "Stránka protokolu zpráv košíku cXML")

## <a name="set-the-extrinsic-elements-for-external-catalog-punchout"></a>Nastavení externích prvků pro externí katalog PunchOut

Když nastavíte pole **Typ protokolu Punchout** na *cXML* pro externí katalog, můžete přidat vlastní externí prvky, které se vloží na správné místo ve zprávě XML požadavku.

Chcete-li přidat externí prvky do externího katalogu, postupujte takto.

1. Přejděte na **Zásobování a zdroje \> Katalogy \> Externí katalogy**.
1. Vyberte příslušný katalog.
1. Na záložce s náhledem **Formát zprávy** v části **Vnější** vyberte **Přidat** a přidejte řádek do mřížky pro každý vnější prvek, který chcete zahrnout. Na každém řádku je třeba nastavit tato pole:

    - **Název** - Zadejte název prvku. Tato hodnota se stane hodnotou atributu **název** pro **Vnější** prvek XML, kterou vytváří každý řádek. Obvykle se ve spolupráci s dodavatelem dohodnete na názvu každého vnějšího prvku.
    - **Hodnota** - Vyberte hodnotu prvku. Tato hodnota se stane hodnotou prvku XML, kterou vytváří každý řádek. K dispozici jsou následující hodnoty:

        - **Uživatelské jméno** – Použijte jméno uživatele, který provádí PunchOut. Toto jméno je přihlašovací jméno pro Supply Chain Management.
        - **Uživatelský e-mail** – Použijte e-mailovou adresu uživatele, který provádí PunchOut. Tato adresa je adresa, kterou si uživatel nastavil na kartě **Obchodní vztah** stránky **Možnosti uživatele**.
        - **Náhodná hodnota** - Použijte jedinečnou náhodnou hodnotu.
        - **Celé jméno uživatele** - Použijte celé jméno kontaktní osoby přidružené k uživateli, který přistupuje k externímu katalogu.
        - **Křestní jméno** - Použijte křestní jméno kontaktní osoby přidružené k uživateli, který přistupuje k externímu katalogu.
        - **Příjmení** - Použijte příjmení kontaktní osoby přidružené k uživateli, který přistupuje k externímu katalogu.
        - **Telefonní číslo** - Použijte primární telefonní číslo kontaktní osoby přidružené k uživateli, který přistupuje k externímu katalogu.

![Nastavení vnějšího prvku.](media/cxml-extrinsics.png "Nastavení vnějšího prvku")

Uživatel nebo správce neuvidí vnější prvky, protože nejsou přidány, dokud uživatel neprovede PunchOut. Budou automaticky vloženy mezi prvky **BuyerCookie** a **BrowserFromPost** ve zprávě s požadavkem na nastavení cXML. Při nastavování externího katalogu je tedy nemusíte nastavovat ručně v XML.

![Vnější prvky přidané do XML.](media/cxml-extrinsics-xml.png "Vnější prvky přidané do XML")

## <a name="create-and-process-a-purchase-order"></a><a name="create-po"></a>Vytvoření a zpracování nákupní objednávky

Když vytvoříte nákupní objednávku pro dodavatele, zdědí nastavení možnosti **Odeslat nákupní objednávku přes cXML** z tohoto dodavatele. Nastavení však zůstává dostupné na záložce s náhledem **Nastavit** v zobrazení **Záhlaví** nákupní objednávky, abyste ho mohli podle potřeby změnit později.

![Nákupní objednávka nastavena na použití cXML.](media/cxml-purchase-order.png "Nákupní objednávka nastavena na použití cXML")

Když vytvoříte nákupní objednávku z nákupní žádanky, která pochází z toku PunchOut, budou vyplněny všechny požadované podrobnosti řádku. Poté můžete ručně přidat řádky nákupní objednávky nebo je zkopírovat z jiných nákupních objednávek. Nezapomeňte nastavit všechna povinná pole. Tato povinná pole zahrnují externí referenční číslo, což je číslo dodavatele, které bude použito ve zprávě cXML.

![Příklad externího referenčního čísla.](media/cxml-line-details.png "Příklad externího referenčního čísla")

Po dokončení vyplnění všech podrobností nákupní objednávky ji nezapomeňte potvrdit. Dokud nebude potvrzena nákupní objednávka, nebude odeslána žádná zpráva. Pro potvrzení nákupní objednávky v podokně akcí na kartě **Nákup** ve skupině **Akce** klikněte na tlačítko **Potvrdit**. 

Po potvrzení nákupní objednávky můžete zobrazit stav potvrzení prostřednictvím deníků **Potvrzení nákupní objednávky**. V podokně Akce na kartě **Nákup** ve skupině **Deníky** zvolte **Potvrzení nákupní objednávky**.

Každá nákupní objednávka může mít mnoho potvrzení. Každé potvrzení je označeno přírůstkovým číslem. Na následujícím obrázku je nákupní objednávka *00000275* a potvrzení je *00000275-1*. Toto číslování odráží standardní funkce Supply Chain Management, kde jsou na základě potvrzení identifikovány změny v nákupní objednávce, a tedy typ zprávy cXML, která by měla být zaslána dodavateli. Jak ukazuje obrázek, stránka **Potvrzení nákupní objednávky** také obsahuje pole **Stav odeslání objednávky** a **Stav dodavatele požadavku na objednávku**. Další informace o různých hodnotách stavu, které se na této stránce mohou zobrazit, najdete v části [Monitorování žádosti o nákupní objednávku](#monitor-po-requests) dále v tomto tématu.

![Stránka potvrzení nákupních objednávek.](media/cxml-po-confirmations.png "Stránka potvrzení nákupních objednávek")

Chcete-li zobrazit více informací o dokumentu, vyberte **Požadavek na objednávku** nad mřížkou.

Stránka **Požadavek na objednávku** obsahuje dvě mřížky. Mřížka v horní části stránky má jeden záznam pro každou nákupní objednávku, která je označena k odeslání. Mřížka na kartě **Historie požadavků na nákupní objednávky** ve spodní části stránky může mít několik záznamů pro vybranou nákupní objednávku, což označuje stav každého potvrzení. Následující obrázek ukazuje nákupní objednávku 00000275 v horní mřížce a dokument 00000275-1 v mřížce na kartě **Historie požadavků na nákupní objednávky**.

![Stránka požadavků na nákupní objednávky.](media/cxml-po-request.png "Stránka požadavků na nákupní objednávky")

Pokud je dávková úloha nastavena a spuštěna, dokument bude odeslán. Změnu stavu můžete zobrazit po odeslání dokumentu. Na následujícím obrázku je pole **Stav odeslání objednávky** nastaveno na _Odesláno_. Pole **Stav dodavatele požadavku na objednávku** je nastaveno na _Potvrzeno_ k označení, že dodavatel obdržel dokument a byl schopen ho přečíst a uložit do svého systému. Mřížka na kartě **Historie požadavků na nákupní objednávky** zobrazuje čas, kdy byl dokument odeslán. Další informace o různých hodnotách stavu, které se na této stránce mohou zobrazit, najdete v části [Monitorování žádosti o nákupní objednávku](#monitor-po-requests).

![Stavové zprávy na stránce požadavku na nákupní objednávku.](media/cxml-po-request-2.png "Stavové zprávy na stránce požadavku na nákupní objednávku")

## <a name="schedule-the-purchase-order-request-batch-job"></a><a name="po-batch"></a>Naplánujte dávkovou úlohu požadavku na nákupní objednávku

Chcete-li aktivovat dávkovou úlohu pro odesílání požadavků na nákupní objednávky, přejděte na **Zásobování a zdroje \>Založit \> Nastavit \> Požadavek na nákupní objednávku** a poté v podokně akcí na kartě **Požadavek na nákupní objednávku** ve skupině **Dávka** vyberte **Odeslat práci** pro otevření dialogového okna **Příprava a odeslání požadavku na nákup**. Toto dialogové okno můžete použít k nastavení opakování, stejně jako to obvykle děláte pro dávkové úlohy v Supply Chain Management. Vyberte interval na základě objemu vaší objednávky. I když můžete dávkovou úlohu spustit každou minutu, je pravděpodobně nejlepší odesílat dávky po celý pracovní den, na základě úseků pro příjem objednávek, které odpovídají plánům vašich dodavatelů.

Například váš dodavatel má zásadu, která uvádí, že všechny objednávky přijaté do 13:00 budou odeslány ve stejný den. V takovém případě možná budete muset dávku spustit jen několikrát během dopoledne, abyste mohli komunikovat všechny své objednávky. Zbývající objednávky budou poté odeslány další den. Toto rozhodnutí je čistě obchodní rozhodnutí. Můžete to zkontrolovat a podle toho nastavit parametry.

Tento proces vyhledá dokumenty požadavků na nákupní objednávku, které mají stav *Čekání*. Pokud máte objednávku, kterou musíte okamžitě odeslat dodavateli, můžete vybrat **Odeslat úlohu** a nastavit možnost **Dávkové zpracování** na *Ne*.

## <a name="monitor-purchase-order-requests"></a><a name="monitor-po-requests"></a>Monitorování požadavků na nákupní objednávku

### <a name="view-the-status-of-a-purchase-order"></a>Zobrazení stavu nákupní objednávky

Když jsou potvrzeny objednávky, které lze odeslat prostřednictvím cXML, přejdou do stavu _Čekání_. Jak bylo popsáno v části [Vytvoření a zpracování nákupní objednávky](#create-po), můžete zobrazit stav nákupní objednávky na stránce **Požadavek na nákupní objednávku**. Každý požadavek na nákupní objednávku může mít jeden z několika stavů, v závislosti na jeho parametrech a datech. Tato část popisuje různé typy stavu a hodnoty, které mohou mít. Tyto informace vám pomohou spravovat problémy a porozumět stavu vašich objednávek.

![Stav nákupní objednávky na stránce požadavku na nákupní objednávku.](media/cxml-monitor-po-request.png "Stav nákupní objednávky na stránce požadavku na nákupní objednávku")

Mřížka v horní části stránky **požadavku na nákupní objednávku** může zobrazit následující stavové hodnoty:

- **Stav odeslání objednávky** - Toto pole může obsahovat jednu z následujících hodnot:

    - **Čekání** - Dokument čeká na odeslání.
    - **Odesláno** - Dokument byl odeslán.
    - **Zastaveno** - Dokument byl označen jako _Zastaveno_ před svým odesláním. (Chcete-li označit dokument jako _Zastaveno_, vyberte **Zastavit** v podokně akcí stránky **Nákupní žádanka**.)
    - **Archivovat** - Dokument byl vymazán. (Chcete-li vyčistit dokument, vyberte **Vyčistit** v podokně akcí stránky **Nákupní žádanka**.)

- **Stav dodavatele požadavku na objednávku** - Toto pole může obsahovat jednu z následujících hodnot:

    - **Čekání** - Dokument čeká na odeslání.
    - **Potvrzeno** - Dokument byl potvrzen jako přijatý dodavatelem. Podrobnou zprávu XML, která je vrácena od dodavatele, můžete zkontrolovat výběrem karty **Odpověď XML** ve spodní části stránky.
    - **Chyba** - Dokument byl odeslán dodavateli, ale došlo k chybě. Chybovou zprávu můžete zkontrolovat výběrem karty **Odpověď XML** ve spodní části stránky.

Mřížka na kartě **Historie požadavků na nákupní objednávky** ve spodní části stránky **Požadavek na nákupní objednávku** může zobrazit následující hodnoty:

- **Typ požadavku na objednávku** - Toto pole může obsahovat jednu z následujících hodnot:

    - **Nový** - Řádek je označen jako nový ihned po potvrzení nákupní objednávky.
    - **Aktualizace** - Pokud již bylo odesláno potvrzení a uznáno prodejcem, bude další potvrzení označeno jako _Aktualizace_. Aktualizace budou odeslány pouze v případě, že je možnost **Odeslat aktualizace nákupních žádanek** nastavena na *Ano* v [globální parametrech cXML](#cxml-parameters).
    - **Odstranit** - Pokud již bylo odesláno potvrzení a uznáno dodavatelem, ale nákupní objednávka je zrušena, bude čekající potvrzení označeno jako _Odstranit_. Odstranění budou odeslána pouze v případě, že je možnost **Odeslat odstranění nákupních žádanek** nastavena na *Ano* v [globální parametrech cXML](#cxml-parameters).

- **Čas požadavku** - Čas, kdy bylo vytvořeno potvrzení objednávky. Můžete porovnat čas požadavku s časem stavu objednávky a určit čas mezi potvrzením a uznáním dodavatele.
- **Stav odeslání objednávky** - Toto pole je stejné jako pole **Stav odeslání objednávky** v horní části stránky. Opakuje se zde, aby bylo snazší zobrazit stav na úrovni potvrzení. Pokud je pole **Typ požadavku na objednávku** nastaveno na *Nový* a před odesláním potvrzení se objednávka znovu potvrdí, je pole **Stav odeslání objednávky** nastaveno na *Archivovat*.
- **Čas stavu objednávky** - Čas, kdy byl naposledy aktualizován záznam historie požadavku na nákupní objednávku. (Aktualizace zahrnují změny stavu.)
- **Stav dodavatele požadavku na objednávky** - Toto pole je stejné jako pole **Stav dodavatele požadavku na objednávky** v horní části stránky. Opakuje se zde, aby bylo snazší zobrazit stav na úrovni potvrzení.
- **Čas opětovného odeslání** - Čas, kdy byl záznam znovu odeslán.
- **Počet opětovných odeslání** - Kolikrát byl záznam znovu odeslán. Vysoké číslo označuje více selhání, a proto může znamenat problém s nastavením dat nebo nastavením dat dodavatele.

### <a name="view-the-xml-for-a-purchase-order-request-message"></a>Zobrazit XML pro zprávu požadavku na nákupní objednávku

Chcete-li zobrazit XML pro zprávu požadavku na nákupní objednávku, vyberte kartu **Text XML požadavku** ve spodní části stránky **Požadavek na nákupní objednávku**. Informace na této kartě mohou být užitečné během testování nebo ověření chyby. Chcete-li informace snáze číst, můžete je zobrazit jako naformátovanou zprávu. Zkopírujte obsah karty do textového souboru a poté jej zobrazte v editoru XML.

![Karta textu XML požadavku.](media/cxml-request-xml-text.png "Karta textu XML požadavku")

### <a name="view-the-details-of-the-vendor-response"></a>Zobrazení podrobností odpovědi dodavatele

Chcete-li zobrazit obsah potvrzení dodavatele nebo chybové odpovědi, vyberte kartu **Odpověď XML** ve spodní části stránky **Požadavek na nákupní objednávku**.

![Karta XML odpovědi.](media/cxml-response-xml.png "Karta XML odpovědi")

## <a name="additional-resources"></a>Další prostředky

- [Nastavení externího katalogu pro funkci PunchOut e-procurement](set-up-external-catalog-for-punchout.md)
- [Použití externích katalogů pro funkci PunchOut eProcurement](use-external-catalogs-for-punchout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]