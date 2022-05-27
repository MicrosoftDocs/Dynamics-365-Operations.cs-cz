---
title: Přehled požadavků na nabídku
description: Toto téma obsahuje přehled požadavků na nabídku. Organizace vygenerují požadavek na nabídku v případě, že chtějí získat konkurenční nabídky od několika dodavatelů, týkající se zboží nebo služeb, které musí nakoupit.
author: GalynaFedorova
ms.date: 10/05/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage, BOMExpandPurchRFQ, PurchRFQReplyFollowupItem, PurchRFQCaseVend, PurchRFQReplyFollowup, PurchRFQCaseAmendmentInfo, PurchRFQReplyFollowupCase, PurchRFQReplyStatus, PurchRFQCaseReplyFields, PurchRFQAddQuestionnaire, PurchRFQAmendmentWizard, PurchRFQReplyTableStatus, PurchRFQReplyTableListPage, PurchRFQCancelWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2154"
- intro-internal
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3de48c03ac73ee164dea0c329b2595db21c841cc
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671947"
---
# <a name="requests-for-quotation-rfqs-overview"></a>Přehled požadavků na nabídku

[!include [banner](../includes/banner.md)]

Toto téma obsahuje přehled požadavků na nabídku. Organizace vygenerují požadavek na nabídku v případě, že chtějí získat konkurenční nabídky od několika dodavatelů, týkající se zboží nebo služeb, které musí nakoupit. V požadavku na nabídku požádejte dodavatele o zadání cen a dodacích lhůt pro zadané množství položek.
Lze také požádat dodavatele, aby určili, zda budou účtovány vedlejší náklady, například přepravní náklady nebo slevy pro velké objednávky či včasnou platbu za fakturu dodavatele.

Proces požadavků na nabídku se skládá z následujících úloh:

1. Vytvoření a odeslání požadavku na nabídku jednomu nebo více dodavatelům.
1. Příjem a zaznamenání nabídek (odpovědí na požadavek na nabídku).
1. Převod přijatých nabídek na nákupní objednávky, nákupní smlouvu nebo nákupní žádanku.

Následující obrázek přehledně znázorňuje průběh procesu požadavku na nabídku.

[![Proces RFQ.](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Případ požadavku na nabídku můžete vytvořit z plánovaných objednávek, z nákupní žádanky nebo ručním zadáním. Případ požadavku na nabídku je základní dokument, který použijete k vystavení požadavku na nabídku pro každého dodavatele.

Po přípravě případu požadavku na nabídku a přidání dodavatelů vyberte **Odeslat** (**Odeslat a publikovat** pro veřejný sektor) v případu požadavku na nabídku. Deník požadavku na nabídku se vygeneruje pro každého dodavatele, kterému jste odeslali požadavek na nabídku. Můžete nakonfigurovat možnosti tisku pro akci Odeslat, aby se buď vytiskla sestava pro každého dodavatele do archivu nebo odeslala sestava na e-mailovou adresu každého dodavatele. Deník požadavku na nabídku pro každého dodavatele lze navíc použít k vytvoření sestavy, kterou lze odeslat nebo později znovu odeslat dodavateli. Také můžete nakonfigurovat akci Odeslat, aby se vygeneroval list odpovědí, který mohou dodavatelé vyplnit.

V tomto tématu je popsán postup zpracování požadavku na nabídku, když se nepoužívá dodavatelská spolupráce. Je-li systém nastaven pro spolupráci dodavatelů, mohou dodavatelé zadávat nabídky přímo v aplikaci Supply Chain Management. Další informace viz [Spolupráce dodavatelů se zákazníky](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations) a [Dodavatelská spolupráce s externími dodavateli](vendor-collaboration-work-external-vendors.md).

Pokud musíte změnit požadavek na nabídku po jeho odeslání, můžete opět odeslat požadavek na nabídku dodavatelům po jeho dokončení s použitím dvou akcí úprav: Vytvoření a Dokončení.

Jakmile obdržíte nabídky e-mailem, můžete s nimi pracovat na stránce **Odpovědi na požadavky na nabídku**.

Pokud je druhá iterace odpovědi vyžadována od dodavatele, zvolte **Vrácení** na stránce **Odpověď na požadavek na nabídku**. Akce Vrácení vytvoří nový deník a sestavu, která bude vytištěna, archivována a odeslána podle nastavení tisku.

Pokud jste přidali kritéria hodnocení do případu požadavku na nabídku, požadavek na nabídku bude mít panel hodnocení, kde můžete zadat výsledky. Celkové hodnocení se zobrazí na RFQ a při porovnání odpovědí na stránce **Porovnat odpovědi**. Na stránce **Porovnat odpovědi** můžete také porovnat jiná data odpovědi, například řádkovou cenu, datum dodání a celkovou cenu.

PO výběru nabídky nebo počtu řádků v nabídce lze přijmout všechny nebo některé řádky a zbývající odmítnout. Vygenerují se deníky přijetí, deníky odmítnutí a příslušné sestavy a budou vytištěny, archivovány a odeslány podle nastavení tisku. Při přijetí nabídky nebo konkrétních řádků v nabídce bude vytvořena nákupní smlouva nebo nákupní objednávka nebo aktualizován nákupní požadavek, v závislosti na typu nákupního požadavku na nabídku. Můžete vytvořit obchodní smlouvu, kterou můžete později použít u všech odpovědí, bez ohledu na to, zda jste je přijali nebo zamítli.

Případ RFQ má dva stavy: nejnižší a nejvyšší. Stav záhlaví požadavku na nabídku můžete zobrazit na stránce **Všechny požadavky na nabídky**. Nejnižší stav je nejméně pokročilou fází jakékoli řádky v požadavku na nabídku a nejvyšší stav je nejpokročilejší fází jakékoli řádky v požadavku na nabídku. Dejme tomu, že případ RFQ se třemi řádky je odeslán dvěma dodavatelům, takže existují dva RFQ po třech řádcích. Všechny řádky jsou **odesláno**. Nyní je zadána nabídka od jednoho z dodavatelů a řádky požadavku na nabídku obdržely stav **přijato**. To znamená, že ze tří řádků případu RFQ jsou všechny **odesláno** pro jeden požadavek na nabídku a **přijato** pro druhý. Nejnižší stav pak bude **Odesláno** a nejvyšší **Přijato.**

Tyto stavy budou popsány podrobněji dále v tomto tématu.

## <a name="setting-up-rfq-functionality"></a>Nastavení funkce RFQ

Než bude možné vytvořit případ požadavku na nabídku, je nutné konfigurovat informace o požadavku na nabídku na stránce **Parametry modulu Zásobování a zdroje**. Při vytváření případu požadavku na nabídku lze zadat výchozí hodnoty, které budou zkopírovány do požadavku na nabídku. Můžete zadat následující výchozí hodnoty:

- Typ nákupu nového požadavku na nabídku: **Nákupní objednávka** nebo **Nákupní smlouva**
- Datum vypršení platnosti a časový posun ode dne vytvoření případu RFQ
- Typ oslovení, který může stanovit výchozí konkrétní metodu hodnocení případu požadavku na nabídku
- Informace o dodání a platební podmínky

Tyto hodnoty lze přepsat pro konkrétní případ požadavku na nabídku.

Také je třeba nakonfigurovat proces změn. V rámci této konfigurace můžete zapnout blokování pole. Při aktivaci uzamykání pole pracovníci zásobování, kteří chtějí změnit požadavek na nabídku, musí nejdříve klepnout na **Vytvořit** v části **Dodatek** na kartě **Nabídka** v případu žádosti o nabídku. Po aktualizaci požadavku na nabídku o dodatek pak musí dokončit proces kliknutím na tlačítko **Finalizovat**. Akce Dokončit vytvoří e-mailovou zprávu, která upozorní dodavatele na doplněný požadavek na nabídku.

Vyberte šablonu, která se má použít pro oznámení e-mailem odeslané dodavatelům na stránce **Parametry modulu Zásobování a zdroje**. Po vytvoření v okně **E-mailové šablony** může šablona obsahovat následující náhradní tokeny:

- %Případ požadavku na nabídku%
- %Důvod pro vrácení nabídky%
- %Důvod pro dodatek%
- %Pořizovatel dodatku%
- %Company%
- %Název případu požadavku na nabídku%
- %Datum a čas vypršení%
- %Date%

Tokeny %Důvod pro vrácení nabídky% a %Důvod pro dodatek% jsou nahrazeny textem, který pracovník zásobování může zadat po dokončení dodatku v průvodci **Dodatek**. Hodnoty pro token %Pořizovatel dodatku% a %Company% jsou automaticky převzaty z RFQ. Token %Date% je nahrazen aktuálním datem.

Jestliže chcete zrušit žádost o cenovou nabídku poté, co byla odeslána musíte to udělat z případu požadavku na nabídku. Pro zrušení se musí použít šablona e-mailu k odeslání oznámení o zrušení kontaktní osobě dodavatele. Je nutné vybrat šablonu na stránce **Parametry modulu Zásobování a zdroje**. Po vytvoření šablony může šablona obsahovat následující náhradní tokeny:

- %Důvod zrušení%
- %Případ požadavku na nabídku%
- %Požadavek na nabídku zrušil/a%
- %Company%
- %Název případu požadavku na nabídku%
- %Date%

Token %Důvod zrušení % se nahradí textem, který může zásobovací pracovník zadat v průvodci **Zrušení**. Token %Date% je nahrazen aktuálním datem.

Pokud chcete použít kódy důvodu v nabídce a označit tak, proč nabídka byla zamítnuta nebo přijata, musíte nastavit kódy důvodu na stránce **Dodavatel – důvody**.

Vzhled vytištěných a uložených dokumentů požadavku na nabídku můžete nakonfigurovat na stránce **Nastavení formuláře** v modulu Zásobování a zdroje.

> [!NOTE]
> U konfigurace veřejného sektoru musíte použít procesu dodatku ke změně požadavku na nabídku, který již byl odeslána. Po odeslání požadavku na nabídku jsou pole uzamčena.
Chcete-li tedy provést změny požadavku na nabídku, je nutné vybrat možnost **Vytvořit** pro zahájení procesu dodatku, jak bylo popsáno výše. Chování uzamčení je ovládáno možností **Zamknout požadavky na nabídku při odeslání** na stránce **Parametry modulu Zásobování a zdroje**. Ve výchozím nastavení je tento parametr nastaven na **Ano** a pro konfiguraci veřejného sektoru toto výchozí nastavení nelze změnit. Z toho vyplývá, že ačkoliv proces dodatku lze zpracovat ručně v konfiguraci neveřejného sektoru, je nutné ho použít pro konfiguraci veřejného sektoru.

Při vytváření případu požadavku na nabídku typu nákupní objednávka a přidávání skladových položek do požadavku na nabídku bude vytvořena také skladová transakce, která má stav příjmu **Příjem nabídky**. Při výpočtu zásob pomocí hlavního plánu jsou použity pouze řádky případu požadavku na nabídku tohoto stavu. Pokud chcete, aby hlavní plán zahrnoval řádky případu požadavku na nabídku jako očekávaný příjem, je nutné konfigurovat toto chování v nastavení hlavního plánování.

Správce nebo zástupce nákupu může vytvořit a spravovat typy oslovení, aby splňovaly požadavky zásobování organizace. Každý typ oslovení může být přidružen k metodě hodnocení. Metody hodnocení obsahují sadu kritérií, kterou lze použít, pokud dosáhnete úspěšné nabídky. Je nutné nastavit typy oslovení, metody hodnocení a kritéria hodnocení na stránce **Typ oslovení** a **Metoda hodnocení**.

## <a name="choose-default-fields-to-include-in-vendor-rfq-reply-forms"></a><a name="default-reply-fields"></a>Výběr výchozích polí, která chcete zahrnout do formulářů pro odpověď dodavatele na požadavku na nabídku

Můžete určit konkrétní typy informací, které chcete obdržet od dodavatelů při odpovědi na požadavky na nabídku. Pole, která označíte jako výchozí, budou zahrnuta v online formuláři poskytnutém pro spolupráci dodavatelů. Jak to nastavit:

1. Pokud jste tak ještě neučinili, použijte stránku [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a povolte funkci *Vybrat pole, která chcete zahrnout do formulářů pro odpověď dodavatele na požadavku na nabídku*.
1. Přejděte na **Zásobování a zdroje > Nastavení > Parametry modulu Zásobování a zdroje**.
1. Otevřete kartu **Požadavek na nabídku**.
1. Vyberte odkaz na pole odpovědí pro **Výchozí požadavky na nabídku** pod nadpisem **Nastavit výchozí hodnoty pro požadavky na nabídku**.
1. Otevře se dialogové okno **Výchozí pole odpovědí v požadavku na nabídku**.
1. Oddíl **Pole požadavku na nabídku obsažená ve formulářích odpovědí dodavatelů na tyto požadavky** obsahuje posuvník pro každé pole, které je k dispozici pro použití v těchto formulářích. Pole nastavená na *Ano* v této části budou zahrnuta (spolu s jejich hodnotami) do formulářů odpovědí na požadavek na nabídku. Nastavte posuvník na *Ne* pro každé pole, u něhož chcete zabránit dodavatelům v zobrazení údajů při kontrole nabídek. To vám umožní zadávat odhadované nebo očekávané hodnoty během zadávání požadavku na nabídku pro interní účely, aniž by prodejce viděl, co bylo zadáno.

Tato nastavení můžete podle potřeby přepsat u jednotlivých požadavků na nabídku.

## <a name="creating-and-sending-an-rfq"></a>Vytvoření a odeslání požadavku na nabídku

Vytvořte případ požadavku na nabídku, vyberte dodavatele, který má zadat nabídku k případu požadavku na nabídku a odešlete požadavek na nabídku dodavatelům. Nastavení tisku můžete použít pro směrování sestavy požadavku na nabídku a listu odpovědí do upřednostňovaného cíle.

Můžete ručně vytvořit případ požadavku na nabídku nákupního typu **Nákupní objednávka** nebo **Nákupní smlouva**.

Jestliže je případ požadavku na nabídku typu **nákupní objednávka**, bude se následující chování lišit od jiných typů případů požadavku na nabídku:

- Při vytvoření řádků případu požadavku na nabídku se vytvoří skladové transakce, které mají stav příjmu **Příjem nabídky**.
- Při přijetí nabídky je vygenerována nákupní objednávka.

Jestliže je požadavek na nabídku typu **nákupní smlouva**, bude se následující chování lišit od jiných typů případů požadavku na nabídku:

- Případ požadavku na nabídku se používá pro dohodu o nákupu určitého množství nebo hodnoty produktu během času. Musíte vybrat rozsah dat, který se týká nákupní smlouvy a jména osoby, která spravuje nákupní smlouvu.
- Při přijetí nabídky je vygenerována nákupní smlouva.

Je-li případ požadavku na nabídku generován na základě nákupního požadavku, typ **Nákupní žádanka** je automaticky přiřazen. Nelze vytvořit ručně případ požadavku na nabídku typu **Nákupní žádanka**.

Případ požadavku na nabídku z nákupního požadavku můžete vytvořit pouze v případě, že je stav nákupního požadavku **Probíhá kontrola** a že jste přiřazeni k provádění další úlohy workflowu. Řádky nákupního požadavku se automaticky aktualizují, jakmile přijmete řádky z nabídek (odpovědí na požadavky na nabídku), které jste získali od dodavatelů. Nelze dokončit, zamítnout, schválit nebo provádět jiné akce u nákupní žádanky, dokud nebude její řádek aktualizován o přijatý řádek RFQ nebo není případ RFQ zrušen.

Pokud vytvoříte případ požadavku na nabídku, můžete vybrat typ oslovení. Typ oslovení určuje sadu kritérií hodnocení, která se používá k získání odpovědí na požadavky na nabídku v případu RFQ.

K případu požadavku na nabídku můžete přiřadit dotazník. Tento dotazník se objeví na všech odpovědích RFQ po odeslání požadavku na nabídku. Vyplnění dotazníku je povinný úkol předtím, než může být nabídka odeslána.

I když jsou k dispozici výchozí hodnoty, můžete podle potřeby změnit nastavení **Pole požadavku na nabídku obsažená ve formulářích odpovědí dodavatelů na tyto požadavky** pro každý jednotlivý případ požadavku na nabídku. Chcete-li tak učinit, vytvořte nebo otevřete konkrétní případ požadavku na nabídku. Poté v podokně akcí otevřete kartu **Nabídka** a v části **Odpovědi** vyberte **Nastavit výchozí hodnoty odpovědí v požadavku na nabídku**. Otevře se dialogové okno **Výchozí požadavek na pole odpovědi na nabídku**, které funguje stejně jako při nastavování výchozích hodnot pro formuláře odpovědí dodavatele na požadavek – s tím rozdílem, že zde provedené změny ovlivní pouze aktuální případ žádosti o nabídku. Podrobnosti o tom, jak tuto funkci povolit a jak funguje, najdete v části [Výběr výchozích polí, která chcete zahrnout do formulářů pro odpověď dodavatele na požadavku na nabídku](#default-reply-fields).

Máte na výběr tři způsoby, jak vybrat dodavatele a přidat jej k případu požadavku na nabídku:

- Přidání dodavatelů po jednom.
- Vyhledání všech dodavatelů, které splňují konkrétní kritéria.
- Automatické přidání všech dodavatelů, kteří byli schváleni pro kategorie zásobování, které se používají v řádcích případu požadavku na nabídku.

Jakmile je případ požadavku na nabídku připraven, zvolte **Odeslat**. Akce Odeslat vytvoří deník a sestavy, které budou vytištěny, archivovány a odeslány podle nastavení tisku.

Pokud jste nastavili pole **Použít dodavatele pro přepočítávání cen** a **Použít informace o položce specifické pro dodavatele** na **Ano** na stránce **Odesílání požadavku na nabídku**, když jste odeslali požadavek na nabídku dodavateli, některé informace pro konkrétní dodavatele budou automaticky doplněny v RFQ pro daného dodavatele.

## <a name="amending-an-rfq-case"></a>Doplnění případu požadavku na nabídku

V některých případech je nutné případ žádosti o nabídku změnit po odeslání. Může být zapotřebí změnit případ požadavku na nabídku, například v případě, kdy byla změněna data dodání, nebo když požadujete další výrobky nebo jiné množství produktů. Proces dodatku můžete nakonfigurovat tak, aby bylo omezení větší nebo menší.

Pokud konfigurujete proces dodatku tak, aby byl více omezující, před úpravou polí v případu požadavku na nabídku, která již byla odeslán, je nutné vybrat **Vytvořit** v případu požadavku na nabídku pro zahájení dodatku. Po dokončení změn je nutné zvolit **Dokončit**. Poté bude provedeni procesem přidání informací pro e-mail, který bude odeslán pro upozornění dodavatelů na změnu. Aktualizovaná sestava požadavku na nabídku, která zahrnuje poznámku o změně, je automaticky přiřazena k e-mailu.

Pokud nakonfigurujete proces dodatku tak, aby byl méně omezující, nemusíte zvolit **Vytvořit** předtím, než bude možné upravit pole v případu požadavku na nabídku, který již byl odeslán. Musíte však ručně přidat poznámku o změně do požadavku na nabídku a odeslat případ znovu. Počítejte s tím, že tento přístup lze použít pouze v případě, že žádná z odpovědí (nabídek) nebyla upravována. Pokud jste zadali odpověď a je ve stavu **Přijato**, tlačítko **Odeslat** není k dispozici. V takovém případě je nutné vybrat **Vytvořit** a pak **Dokončit**, jako to musíte provést ve více omezujícím procesu. Odpověď se potom resetuje, aby odrážela změny případu požadavku na nabídku.

Pokud dodavatelé používají rozhraní dodavatelské spolupráce k zadávání nabídek, musíte vždy použít proces dodatku, abyste informovali dodavatele o změnách případu požadavku na nabídku. Tento proces pomáhá zabránit situaci, kdy dodavatelé vytvoří nabídku na zastaralý případ požadavku na nabídku, zatímco probíhá jejich nabídka. Další informace o dodavatelské spolupráci naleznete v tématu [Dodavatelská spolupráce s externími dodavateli](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-external-vendors).

Pokud chcete pozvat další dodavatele k nabídce a nebyly provedeny žádné změny případu požadavku na nabídku, lze použít tlačítko **Odeslat**. Dodavatele, které jste přidali, se zobrazí na stránce **Odeslat** a dostanou pozvání e-mailem.

## <a name="receiving-and-registering-rfq-replies"></a>Příjem a registrace odpovědí na RFQ

Při odeslání požadavku na nabídku se automaticky vytvoří list odpovědi. Jakmile dostáváte nabídky v požadavku na nabídku, musíte je zadat prostřednictvím stránky **Požadavek na nabídku** kliknutím na akci **Upravit odpověď RFQ**. To vám umožní zadat informace o nabídce ve formě vyhrazený nabídky. Zpočátku bude **průběh odpovědi** **Nezahájeno**. Po klepnutí na tlačítko **Upravit odpověď RFQ** bude stav pokroku **Aktualizuje se nákupčí**, dokud nabídka nebude odeslána. Klepněte na tlačítko **odeslat** poté, co zadáte informace nabídky. Stav průběhu odpovědi se změní na **odesláno nákupčím.** Podobně platí, že když je povolena spolupráce s dodavatelem, bude se **průběh odpovědi** aktualizovat s tím, jak se dodavatel na nabídce podílí. Stav se pak změní z **Aktualizuje se dodavatel** na **odeslané dodavatelem**. Při odeslání nabídky je vytvořen deník jako **přijato**. Odpověď (nabídka) musí být odeslána za účelem registrace jako přijaté, a teprve poté ji lze dále upravovat jako přijatou nebo odmítnutou.

Pokud potřebujete aktualizovat nabídku, je třeba projít stejným procesem, jaký je uveden výše, a znovu odeslat.

Všimněte si, že úprava formuláře **Požadavek na nabídku** je povolena pouze pro informace, které se týkají zpracování nabídky, ne pro zadávání nabídky. Zadejte nebo upravte nabídku klepnutím na **Upravit odpověď na požadavek na nabídku.**

Při zadávání údajů z nabídky a pokud to umožňuje případ požadavku na nabídku pro alternativní řádky, můžete přidat alternativní řádky pro řádky, které mají pouze kategorie zásobování a žádnou zadanou katalogovou položku. Kliknutím na tlačítko **přidat alternativu** přidáte alternativní řádky.

Pokud jste zadali odpověď, ale požadujete novou nabídku od dodavatele, můžete vrátit RFQ. Vygeneruje se nový deník a sestava, které lze odeslat dodavateli.

Přehled všech požadavků na nabídku a jejich stavy: **Odesláno, Převzato, Přijato, zamítnuto, zrušeno, odmítnuto** naleznete na stránce **Zpracování požadavku na nabídku**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Přijetí a odmítnutí nabídek a přenos přijatých nabídek do podřízených dokumentů

Poté, co jste vybrali nejlepší nabídku, například nabídku, jež nabízí nejlepší celkovou cenu, nabídky přijměte. V nabídce můžete přijmout některé řádky a jiné zamítnout.
Lze také přijímat řádky od různých dodavatelů. Počítejte s tím, že pokud přijmete některé řádky, budete vyzváni k odmítnutí všechny ostatních řádků. Z toho vyplývá, že pokud chcete přijmout další řádky, musíte zvolit **Zrušit** po zobrazení výzvy. Stav odpovědi na požadavek na nabídku pro každého dodavatele, od kterého přijímáte nabídky nebo řádky, je aktualizován na **Přijato**.

Potřebujete-li, při přípravě nákupní objednávky nebo nákupní smlouvy, přidat další řádek do požadavku na nabídku, můžete to provést klepnutím na tlačítko **přidat řádek** na řádku mřížky stránek **požadavek na nabídku**. Tento řádek můžete zobrazit a upravit pouze na stránce **Požadavek na nabídku**. Zobrazí se na stránce nabídky při přijetí.

Při přijetí nabídky nebo jedné či více řádek v nabídce se automaticky vytvoří nákupní objednávka nebo nákupní smlouva. Poté můžete odmítnout nabídky od všech ostatních dodavatelů.

V odpovědi můžete přidat kód důvodu vysvětlující příčinu přijetí nebo odmítnutí nabídky.

Pokud přijmete nabídku typu **Nákupní žádanka**, budou řádky nákupní žádanky aktualizovány o následující informace, které odrážejí informace na přijaté nabídce:

- Jedn. cena
- Procento slevy
- Částka slevy
- Doprovodné nákupní náklady
- Náklady pro řádek
- Dodavatel
- Externí hodnota
- Externí popis

Následující tabulka obsahuje změny stavu požadavku na nabídku při přijetí a odmítnutí nabídek od dodavatelů.

## <a name="statuses--highest-and-lowest"></a>Stavy – nejnižší stav a nejvyšší stav.

Na kartě Dodavatel případu požadavku na nabídku se zobrazí řádky s nejvyšším a nejnižším stavem pro určitého dodavatele. Když je přidán dodavatel a dosud nebyly odeslány žádné řádky, je nejnižší i nejvyšší stav <strong>Vytvořeno</strong>. Když je poptávka odeslána prodejci se všemi řádky, bude stav těchto dvou řádků <strong>Odesláno</strong>. Pokud jsou některé řádky v nabídce od dodavatele přijaty a jiné odmítnuty ostatní, odmítnuté řádky dostanou nejnižší stav, což je <strong>Odmítnuto</strong>, a u přijatých řádek se zobrazí nejvyšší stav, což je <strong>Přijato</strong>.

V řádcích případu požadavku na nabídku se zobrazí nejvyšší a nejnižší stav na řádek pro všechny dodavatele. Pokud jste odeslali řádek všem dodavatelům v případu požadavku na nabídku a nikdo ještě neodpověděl, nejvyšší i nejnižší stav je **odesláno.** Když reaguje alespoň jeden dodavatel, nejvyšší stav se změní na **přijato**. Při přidání nového dodavatele k případu se nejnižší stav změní na **vytvořeno**

Nejvyšší a nejnižší stav v případu požadavku na nabídku je agregací stavu na kartě \<Dodavatele a Řádky.

Stavy jsou řazeny nejvyšší od nejnižšího k nejvyššímu následujícím způsobem: vytvořeno, odesláno, přijato, zamítnuto, přijetí, odmítnutí, zrušení.

Následující tabulka uvádí změny stavu případu požadavku na nabídku při vytvoření případu FRQ s řádky a násleným odesáním dodavatelům.

| **Akce**                                | **Nejnižší stav řádky případu požadavku na nabídku** | **Nejvyšší stav řádky případu požadavku na nabídku** | **Nejnižší stav řádku případu požadavku na nabídku** | **nejvyšší stav řádku případu požadavku na nabídku** |
|-------------------------------------------|----------------------------|-----------------------------|---------------------------------|----------------------------------|
| Vytvoření záhlaví a řádku RFQ.      | Vytvořeno                    | Vytvořeno                     | Vytvořeno                         | Vytvořeno                          |
| Odeslání žádostí o nabídku všem dodavatelům v případu RFQ. | Odesláno                       | Odesláno                        | Odesláno                            | Odesláno                             |
| Přidejte jiného dodavatele.                       | Vytvořeno                    | Odesláno                        | Vytvořeno                         | Odesláno                             |
| Odešlete požadavek na nabídku druhému dodavateli.        | Odesláno                       | Odesláno                        | Odesláno                            | Odesláno                             |

Všechny řádky v RFQ vztahující se k případu požadavku na nabídku budou mít stav **odesláno**.

Následující tabulka uvádí změny stavu požadavku na nabídku při příjmu nabídek a registraci informací na listu pro odpovědi na požadavek na nabídku.

| **Akce**                                               | **Nejnižší stav napříč všemi řádky všech RFQ** | **Nejvyšší stav napříč všemi řádky všech RFQ** | **Nejnižší stav záhlaví případu požadavku na nabídku** | **Nejvyšší stav záhlaví případu požadavku na nabídku** | **Nejnižší stav řádku případu požadavku na nabídku** | **nejvyšší stav řádku případu požadavku na nabídku** |
|----------------------------------------------------------|------------------------------------------------|-------------------------------------------------|-----------------------------------|------------------------------------|---------------------------------|----------------------------------|
| Zaregistrujte jednu nabídku RFQ od dodavatele a uložte ji.        | Odesláno                                           | Přijato                                        | Odesláno                              | Přijato                           | Odesláno                            | Přijato                         |
| Zaregistrujte druhou nabídku od dodavatele v RFQ a uložte ji. | Přijato                                       | Přijato                                        | Přijato                          | Přijato                           | Přijato                        | Přijato                         |


V následujícím příkladu se můžete podívat na nejvyšší a nejnižší stav v požadavku na nabídku v případě, že byla získána jedna nabídka a ostatní přijaty. Když je získaná nabídka zamítnuta, nejnižší stav se změní z přijato na odmítnuto v záhlaví a na řádku případu požadavku na nabídku.


|            <strong>Akce</strong>             | <strong>Nejnižší stav napříč všemi řádky všech RFQ</strong> | <strong>Nejvyšší stav napříč všemi řádky všech RFQ</strong> | <strong>Nejnižší stav záhlaví případu požadavku na nabídku</strong> | <strong>Nejvyšší stav záhlaví případu požadavku na nabídku</strong> | <strong>Nejnižší stav řádku případu požadavku na nabídku</strong> | <strong>nejvyšší stav řádku případu požadavku na nabídku</strong> |
|------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------|-------------------------------------------------|----------------------------------------------|-----------------------------------------------|
| Přijměte jednu z nabídek. (nebo alespoň jeden řádek) |                          Přijato                           |                           Akceptováno                           |                    Přijato                    |                    Akceptováno                     |                   Přijato                   |                   Akceptováno                    |
|           Odmítněte všechny ostatní nabídky.           |                          Odmítnuto                           |                           Akceptováno                           |                    Odmítnuto                    |                    Akceptováno                     |                   Odmítnuto                   |                   Přijato                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]