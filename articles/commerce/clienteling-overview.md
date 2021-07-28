---
title: Přehled clientelingu
description: Toto téma obsahuje přehled nových funkcí clientelingu dostupných v aplikaci obchodu.
author: bebeale
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom:
- "260624"
- intro-internal
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 598145bccadbeb44d33adb96388f6af5a8a45f5d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352681"
---
# <a name="clienteling-overview"></a>Přehled clientelingu

[!include [banner](includes/banner.md)]


Mnoho maloobchodních prodejců, zejména špičkových specializovaných prodejců špičkových chce, aby jejich zaměstnanci obchodů vytvářeli dlouhodobé vztahy se svými klíčovými zákazníky. Očekává se, že zaměstnanci obchodů znají, co mají zákazníci rádi, nákupní historii, preference produktů a důležitá data, jako jsou například výročí a narozeniny. Zaměstnanci obchodů potřebují místo, kde mohou tyto informace zaznamenat a snadno je najít v případě potřeby. Pokud jsou tyto informace k dispozici v jediném zobrazení, zaměstnanci obchodů mohou snadno cílit na zákazníky, kteří vyhovují konkrétním kritériím. Mohou například najít všechny zákazníky, kteří dávají přednost kabelkám, nebo zákazníky s důležitými událostmi, jako jsou například narozeniny nebo výročí.

## <a name="client-book"></a>Kniha klienta

V aplikaci Microsoft Dynamics 365 Commerce mohou maloobchodní prodejci použít funkci klientské knihy, aby pomohli zaměstnancům obchodu vytvářet dlouhodobé vztahy s klíčovými zákazníky.

Klientská kniha obsahuje karty zákazníků, které zobrazují kontaktní informace každého odběratele, spolu se třemi dodatečnými vlastnostmi definovanými maloobchodníky a konfigurovanými v Headquarters. Maloobchodní prodejci mohou rozhodnout o třech nejdůležitějších skutečnostech, které by měl zaměstnanec obchodu vědět o zákaznících. Například maloobchodní prodejce šperků může chtít zahrnout významná data, jako jsou například výročí nebo narozeniny, protože při těchto příležitostech kupují lidé více šperků. Podobně může maloobchodní prodejce módy chtít zahrnout preferované nákupní zájmy a obchodní značky zákazníka.

Klientská kniha také umožňuje zaměstnancům obchodu filtrovat seznam, aby zobrazoval pouze zákazníky splňující určitá kritéria. Například do obchodu byla dodána nová kolekce obuvi a zaměstnanec obchodu chce informovat zákazníky, kteří chtějí nakupovat obuv. V takovém případě může zaměstnanec obchodu filtrovat knihu klienta tak, aby nalezl relevantní zákazníky, a poté provést další akci.

Pokud někteří zákazníci z nějakého důvodu nebudou nadále považováni za klíčové zákazníky, a proto by neměli být plně spravováni, může je zaměstnanec z knihy klienta odebrat.

Někteří maloobchodní prodejci nechtějí spravovat odběratele na úrovni zaměstnance obchodu. Místo toho chtějí spravovat seznam klíčových zákazníků na úrovni obchodu. Tito maloobchodní prodejci mohou zobrazit zákazníky z knih klientů obchodu. Použitím této možnosti mohou maloobchodní prodejci zobrazit zákazníky z klientských knih všech zaměstnanců obchodu, jejichž adresář se shoduje s adresářem aktuálního obchodu. Tímto způsobem, pokud zaměstnanec obchodu pracuje ve vícero obchodech právnické osoby, zobrazuje kniha klientů zákazníky ze všech obchodů. Tato funkce podporuje další možnosti. Zákazníci mohou být například opětovně přiřazeni od jednoho zaměstnance obchodu k druhému. Tato možnost je užitečná při převodu zaměstnance obchodu nebo jeho opuštění společnosti.

Každý zaměstnanec obchodu může mít jednu klientskou knihu pro jednu právnickou osobu a zaměstnanci obchodu do ní mohou přidávat jednoho nebo více zákazníků. V aplikaci Commerce lze jednotlivé zákazníky přidat pouze do jedné klientské knihy. Společnost Microsoft však plánuje přidání funkce, která umožní přidání jednoho zákazníka do několika klientských knih.

> [!NOTE]
> Na rozdíl od vyhledávání odběratele klientská kniha nefiltruje záznamy o zákaznících na základě adresáře obchodu.

## <a name="activities-and-notes"></a>Aktivity a poznámky

Online kanály poskytují prodejcům způsoby, jak se dozvědět o zákaznických preferencích, aniž by bylo nutné, aby zákazníci tyto informace výslovně zadali. Pokud naopak zákazníci komunikují se zaměstnanci v obchodě, budou explicitně sdílet informace o svých preferencích. Tyto informace lze bohužel po ukončení prodeje ztratit. Je-li však tato informace zaznamenána, může pomoci prodejcům lépe pochopit zákazníky a poskytnout jim lepší doporučení a zlepšit celkové možnosti nakupování.

Chcete-li zachytit důležité informace, které zákazníci sdílejí, mohou zaměstnanci obchodu použít nejen atributy knih klientů, ale také používat funkci aktivit a poznámek. Maloobchodní prodejci mohou konfigurovat typy aktivit (například informace o návštěvě obchodu, e-mailové adresy, telefonní číslo a události). Aktivity, které vytváří zaměstnanci obchodu, lze zobrazit ve formátu časové osy na pokladním místě (POS). Lze je také zobrazit na kartě **Činnosti** na stránce **Všichni zákazníci \> Obecné** v Headquarters.

Zaměstnanci obchodu mohou rovněž používat poznámky k záznamu obecných informací o zákazníkovi, které mohou být odkazovány před každou interakcí. Tyto poznámky jsou uloženy v Headquarters a lze je zobrazit v profilu zákazníka nebo na stránce Podrobnosti o zákazníkovi v kontaktním středisku.

> [!NOTE]
> V současné době může všechny poznámky a aktivity zobrazit libovolný zaměstnanec obchodu, který pracuje pro právnickou osobu a může zobrazit stránky s podrobnostmi o odběrateli. Poznámky a aktivity nejsou omezeny na zaměstnance obchodu, který přidal zákazníka do knihy klientů.

## <a name="integration-with-dynamics-365-customer-insights"></a>Integrace s aplikací Dynamics 365 Customer Insights

Při použití aplikace Dynamics 365 Customer Insights mohou maloobchodní prodejci agregovat data z různých systémů, které zákazníci používají pro interakci se značkou maloobchodního prodejce. Poté mohou pomocí těchto dat vygenerovat jediné zobrazení zákazníka a odvodit přehledy. Integrace aplikace Customer Insights s aplikací Commerce umožňuje maloobchodním prodejcům vybrat jedno nebo více měřítek, které mají být zobrazeny na kartě zákazníka v klientské knize. Maloobchodníci mohou například použít data v Customer Insights k výpočtu pravděpodobnosti odchodu zákazníka a k definování „další nejlepší akce“. Jsou-li tyto hodnoty definovány jako měřítka, lze je zobrazit na kartě zákazníka a poskytnout důležité informace pro zaměstnance obchodu. Další informace o Customer Insights naleznete v dokumentaci [Dynamics 365 Customer Insights](/dynamics365/ai/customer-insights/overview). Další informace o měřítkách naleznete v tématu [Měřítka](/dynamics365/ai/customer-insights/pm-measures).

## <a name="set-up-clienteling"></a>Nastavení clientelingu

Chcete-li ve vašem prostředí zapnout funkci clientelingu, postupujte podle následujících kroků.

1. V pracovním prostoru **Správa funkcí** filtrujte funkce podle modulu **Maloobchodní a velkoobchodní prodej**.

    ![Clienteling v seznamu funkcí pro modul Commerce.](./media/Enable_clienteling.png "Clienteling v seznamu funkcí pro modul Maloobchodní a velkoobchodní prodej")

2. Zapněte funkci **Clienteling** volbou **Povolit nyní**.
3. Na stránce **Parametry Commerce** na kartě **Číselná řada** vyberte řádek identifikátoru **Identifikátor knihy klienta**. V poli **Kód číselné řady** vyberte číselnou řadu. Systém použije tuto číselnou řadu k přiřazení ID ke klientským knihám.
4. Zvolte **Uložit**.
5. Vytvořte novou skupinu atributů obsahující atributy, které chcete zaznamenat pro zákazníky, kteří jsou spravováni v klientských knihách. Pokyny naleznete v tématu [Atributy a skupiny atributů](./attribute-attributegroups-lifecycle.md).

    - Definujte požadované atributy jako **Lze upřesnit**. Tento atribut pak mohou zaměstnanci obchodu použít k filtrování knihy klienta.
    - Nastavte pořadí zobrazení těchto atributů. Toto pořadí zobrazení určuje, které atributy mají být zobrazeny na kartě zákazníka v klientské knize. Pořadí zobrazení 1 je považováno za vyšší než pořadí zobrazení 2. Proto atribut, který má pořadí zobrazení 1, bude zobrazen před atributem, který má pořadí zobrazení 2.

    > [!NOTE]
    > Customer Insights můžete zpřístupnit na stejné stránce. Pro účely ověření je však nutné vytvořit ID aplikace Azure a tajný klíč. (Informace o požadavcích naleznete v další čísti tohoto tématu [Zapnutí integrace Customer Insights s aplikací Commerce](#turn-on-the-integration-of-customer-insights-with-commerce).) Je-li zapnuta aplikace Customer Insights a vyberete jedno nebo více měřítek, které mají být zobrazeny na kartě zákazníka, tato měřítka se zobrazí jako první. Dále budou zobrazeny skupiny atributů klientských knih na základě pořadí zobrazení. Pokud například vyberete dvě měřítka z Customer Insights, zobrazí se na kartě zákazníka tao dvě měřítka a jeden atribut v klientské knize. (Zobrazený atribut klienta knihy bude atribut, který má nejvyšší pořadí zobrazení.)

6. Na stránce **Parametry Commerce** na kartě **Clienteling** v poli **Skupina atributů klientských knih** vyberte skupinu atributů, kterou jste právě vytvořili.

    ![Vybraná skupina atributů knihy klientů.](./media/Client%20book%20attributes.png "Vybraná skupina atributů knihy klientů")

7. Chcete-li zaznamenat aktivity, které se vyskytují v POS, definujte typy aktivit stránce **Typ aktivity** (**Retail and Commerce \> Zákazníci \> Typy aktivit**).

    > [!NOTE]
    > Typy aktivit jsou při prvním volání v reálném čase vyžádány Commerce Scale Unit. Jakmile jsou tyto aktivity načteny, jsou uloženy do mezipaměti několik hodin. Pokud změníte typy aktivit, počkejte, dokud mezipaměť nebude platná. Případně můžete službu Commerce Scale Unit restartovat i v jiných než provozních prostředích.

8. Přidejte dvě tlačítka do příslušného rozvržení obrazovky POS, aby si zaměstnanci obchodu mohli prohlédnout svou vlastní klientskou knihu a knihu klienta obchodu. (Klientské knihy obchodů zahrnují klienty ze všech klientských knih všech zaměstnanců obchodu, kteří sdílejí adresář s obchodem.) Odpovídající operace se nazývají **zobrazení odběratelů v klientské knize** a **zobrazení odběratelů z klientských knih obchodu**. K dispozici jsou tři další operace související s klientskými knihami. Tyto operace určují, kteří zaměstnanci obchodu mohou přidávat, odebírat a přeřazovat zákazníky z klientské knihy. Nazývají se **Přidat zákazníka do klientské knihy**, **Odebrat zákazníka z klientské knihy** a **Opětovně přiřadit zákazníka do klientské knihy**.
9. Spusťte následující úlohy plánu distribuce: 1040, 1150, 1110 a 1090.

Po dokončení tohoto postupu může zaměstnanec obchodu otevřít stránku podrobnosti o odběrateli v POS a přidat odběratele do své klientské knihy, zobrazit a zaznamenat aktivity a poznámky pro odběratele a zaměřit se na zákazníky pomocí atributů odběratele a knihy klienta k filtrování knihy klienta. Následující obrázek znázorňuje příklad knihy klienta.

![Příklad knihy klienta.](./media/client_book.png "Příklad knihy klienta")

## <a name="turn-on-the-integration-of-customer-insights-with-commerce"></a>Zapnutí integrace Customer Insights s aplikací Commerce

Chcete-li zapnout integraci Customer Insights s aplikací Commerce, musíte se ujistit, že máte aktivní instanci Customer Insights v klientovi, kde je zřízena aplikace Commerce. Je také nutné mít uživatelský účet Azure Active Directory (Azure AD), který má předplatné Azure.

Pro nastavení integrace postupujte následujícím způsobem.

1. Na webu Azure Portal zaregistrujte novou aplikaci a poznamenejte si název aplikace, ID aplikace a tajný klíč. Tyto informace budou použity pro autentizaci mezi službami mezi Commerce a Customer Insights. Poznamenejte si tajný kód bezpečně, protože bude nutné jej uložit do trezoru klíčů. V následujícím příkladu použijte CI_Access_name, CI_Access_AppID, CI_Access_Secret jako název aplikace, ID aplikace a tajný kód. Další informace naleznete v tématu [Rychlý start: registrace aplikace pomocí platformy identity Microsoft](/azure/active-directory/develop/quickstart-register-app).

    > [!IMPORTANT]
    > Proveďte kroky, abyste si před vypršením platnosti mohli změnit tajný klíč. V opačném případě dojde k neočekávanému zastavení integrace.

2. Přejděte do instance Customer Insights a vyhledejte název aplikace vytvořené výše (v tomto příkladu „CI_Access_name“).
3. Vytvořte trezor klíčů Azure a poznamenejte si název a adresu URL (v tomto příkladu „KeyVaultName“, „KeyVaultURL“). Pokyny naleznete v tématu [Rychlý start: nastavení a načtení tajného klíče z Azure Key Vault pomocí portálu Azure](/azure/key-vault/quick-create-portal).
4. Uložte tajný kód (v tomto příkladu „CI_Access_Secret“) do trezoru. Když je tento tajný kód uložen v trezoru, získá název. Poznamenejte si název tajného kódu (v tomto příkladu „SecretName“).
5. Chcete-li získat přístup k tajnému kódu z Azure Key Vault, musíte vytvořit jinou aplikaci s ID aplikace a tajným kódem (v tomto příkladu „KeyVault_Access_AppID“ a „KeyVault_Access_Secret“). Poznamenejte si tajemství bezpečně, protože se již nebude znovu zobrazovat.
6. Dále musíte aplikaci udělit oprávnění pro přístup k trezoru klíčů z Commerce pomocí API. Přejděte na stránku aplikace v portálu Azure. V části **Spravovat** vyberte **Oprávnění API**. Přidejte oprávnění k přístupu **Azure key vault**. U tohoto oprávnění vyberte **Zásady přístupu**. Vyberte šablonu jako **Správa tajného kódu** a vyberte možnost **Získat**, **Seznam**, **Dešifrovat** a **Šifrovat**. 
5. V programu Commerce Headquarters přejděte do **Správa systému \> Nastavení \> Parametry úložiště klíčů** a zadejte požadované informace o úložišti klíčů. Poté v poli **Klient úložiště klíčů** zadejte ID aplikace, které jste použili v kroku 4, aby aplikace Commerce mohla používat tajné klíče v úložišti klíčů.
6. Chcete-li přidat aplikaci vytvořenou v kroku 1 do seznamu bezpečných aplikací (někdy označovaných jako bezpečný seznam), přejděte na Customer Insights a vyberte přístup **Zobrazení** k aplikaci. Pokyny naleznete v tématu [Oprávnění](/dynamics365/ai/customer-insights/pm-permissions).
7. Na stránce **Správa systému > Nastavení > Parametry trezoru klíčů** na Commerce HQ upravte pole, jak je popsáno níže: 

- **Key Vault url**: "KeyVaultURL" (z kroku 3 výše).
- **Key Vault client**: "KeyVault_Access_AppID" (z kroku 5 výše).
- **Key Vault secret key**: "KeyVault_Access_Secret" (z kroku 5 výše).
- V části **Tajné klíče**:
    - **Název** : Libovolný název, například „CISecret“.
    - **Popis** : Jakákoli hodnota.
    - **Tajný kód** : **vault**://<Name of key vault>/<name of secret>> V tomto příkladu to bude „vault://KeyVaultName/SecretName“.

Po úpravě polí vyberte **Ověřit**, aby bylo zajištěno, že k tajnému kódu bude mít přístup aplikace Commerce.

8. V Commerce na stránce **Parametry Commerce** na kartě **Clienteling** na pevné kartě **Dynamics 365 Customer Insights** nastavte **ID aplikace** na „CI_Access_AppID“ (z kroku 1 výše). Jako **Název tajného kódu** vyberte název tajného kódu zadaný v kroku 7 výše („CISecret“). Nastavte možnost **Povolit Customer Insights** na **Ano**. Pokud je instalace z nějakého důvodu neúspěšná, zobrazí se chybová zpráva a tato možnost bude nastavena na **Ne**. 

V Customer Insights můžete mít více prostředí, jako je například testovací a provozní prostředí. Do pole **ID instance prostředí** zadejte příslušné prostředí. V poli **Alternativní ID odběratele** zadejte vlastnost v Customer Insights, která je mapována na číslo účtu odběratele. (V Commerce je číslo zákaznického účtu ID zákazníka.) Zbývající tři vlastnosti jsou míry, které se zobrazí na zákaznické kartě v knize klientů. Můžete vybrat až tři měřítka, která se mají zobrazit na kartě zákazníka. Není však nutné vybírat žádné míry. Jak již bylo zmíněno dříve, systém nejprve zobrazí tyto hodnoty a poté zobrazí hodnoty pro skupinu atributů knihy klientů.


[!INCLUDE[footer-include](../includes/footer-banner.md)]