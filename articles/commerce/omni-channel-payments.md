---
title: Přehled omnikanálových plateb
description: Toto téma poskytuje přehled omnikanálových plateb v aplikaci Dynamics 365 Commerce.
author: rubendel
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 8.1.3
ms.openlocfilehash: 3fe64dad3c60560363428d76566d910868b87111
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244904"
---
# <a name="omni-channel-payments-overview"></a>Přehled omnikanálových plateb

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled omnikanálových plateb v aplikaci Dynamics 365 Commerce. Obsahuje obsáhlý seznam podporovaných scénářů, informace o funkcích, nastavení a řešení problémů a popis některých typických problémů.

## <a name="key-terms"></a>Klíčové podmínky

| Termín | Popis |
|---|---|
| Token  | Řetězec dat, který platební procesor poskytuje jako referenční. Tokeny mohou představovat čísla platebních karet, autorizace plateb a předchozí zachycená platby. Tokeny jsou důležité, protože pomáhají zachovat citlivá data z prodejního systému (POS). Někdy se také nazývají *reference*. |
| Token karty | Token, který platební procesor poskytuje pro uložení v systému POS. Token karty může používat pouze obchodník, který jej obdrží. Tokeny karty se někdy označují také jako *reference karty*. |
| Token (autorizace) platby | Jedinečný identifikátor, který platební proces poskytuje jako součást odpovědi, kterou odešle do systému POS poté, co systém POS provede požadavek na autorizaci. Autorizační token lze později použít v případě, že je procesor vyzván k provádění akcí, jako je například stornování nebo zrušení autorizace. Používá se však nejčastěji k zaznamenání finančních prostředků při splnění objednávky nebo finalizaci transakce. Tokeny autorizace se někdy označují také jako *reference autorizace*. |
| Token zachycení | Reference, kterou platební procesor poskytuje systému POS při finalizaci nebo zachycení platby. Token zachycení lze poté použít pro odkazování na záznam platby v následných operacích, jako je například požadavek na refundaci. | 
| Karta není přítomna | Termín, který odkazuje na platební transakce, u nichž není zobrazena fyzická karta. Tyto transakce mohou například nastat ve scénářích elektronického obchodu nebo kontaktních středisek. Pro tyto transakce jsou informace související s platbou zadány ručně na webu elektronického obchodu, v toku kontaktního centra nebo na POS nebo v platebním terminálu. |
| Karta je přítomna | Termín, který odkazuje na platební transakce, ve kterých se zobrazuje a používá v platebním terminálu, který je připojen k systému Microsoft Dynamics 365 POS. |

## <a name="overview"></a>Přehled

Pojem *omnikanálové platby* obecně popisuje schopnost vytvořit objednávku v jednom kanálu a splnit ji v jiném kanálu. Klíčem pro podporu omnikanálové platby je zachování platebních detailů spolu ze zbytkem detailů objednávky a následné použití těchto platebních detailů, když je objednávka stažena nebo zpracována v jiném kanálu. Klasickým příkladem je scénář "koupit online, vyzvednout v obchodě". V tomto scénáři jsou údaje o platbě doplněny při vytvoření objednávky online. Poté jsou v POS odvolány, aby v okamžiku vyzvednutí byla stržena platba z platební karty zákazníka. 

Všechny scénáře popsané v tomto tématu lze implementovat pomocí standardní sady Software Development Kit (SDK) plateb dodávané s aplikací Commerce. Konektor [Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) poskytuje přednastavenou implementaci každého scénáře, který je zde popsán. 

### <a name="prerequisites"></a>Předpoklady

Každý scénář, který je popsán v tomto tématu, vyžaduje platební konektor, který podporuje omnikanálové platby. Konektor Adyen lze také použít ihned po vybalení, protože podporuje scénáře, které jsou k dispozici v sadě SDK plateb. Další informace o tom, jak implementovat konektory platby, a obecné informace o sadě SDK naleznete na stránce [Maloobchod pro profesionály IT a vývojáře](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors).

#### <a name="supported-versions"></a>Podporované verze

Schopnosti omnikanálové platby, které jsou popsány v tomto tématu, byly vydány v rámci Microsoft Dynamics 365 for Retail verze 8.1.3. 

#### <a name="card-present-and-card-not-present-connectors"></a>Konektory "Přítomná karta" a "Nepřítomná karta"

Sada SDK plateb spoléhá na dvě sady aplikačních programovacích rozhraní (API) pro platby. První sada rozhraní API je pojmenovaná **iPaymentProcessor**. Používá se k implementaci konektorů pro platby "karta není přítomna", které lze použít v kontaktních střediscích a na platformě elektronického obchodování Microsoft Dynamics. Další informace o rozhraní **iPaymentProcessor** naleznete v dokumentu white paper [Implementace platebního konektoru a platebního zařízení](https://download.microsoft.com/download/e/2/7/e2735c65-1e66-4b8d-8a3c-e6ef3a319137/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device_update.pdf), který se věnuje platbám. 

Druhá sada rozhraní API je pojmenovaná **iNamedRequestHandler**. Podporuje implementaci integrace plateb "karta přítomna", která používá platební terminál. Další informace o rozhraní **iNamedRequestHandler** získáte v části [Vytvoření integrace platby pro platební terminál](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension). 

### <a name="setup-and-configuration"></a>Instalace a konfigurace

Jsou požadovány následující součásti a kroky nastavení:

- **integrace eCommerce:** Podpora scénářů, jejichž pořadí pochází z online výlohy, vyžaduje integraci s aplikací Commerce. Další informace o sadě Retail e-Commerce SDK naleznete v tématu [sada SDK (Software Development Kit) platformy elektronického obchodování](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk). V ukázkovém prostředí podporuje referenční výkladní skříň scénáře omniplateb. 
- **Konfigurace online plateb:** nastavení online kanálu musí obsahovat platební konektor, který byl aktualizován pro podporu omniplateb. Případně lze použít konektor pro platby po vybalení. Informace o konfiguraci konektoru plateb Adyen pro online obchody naleznete v tématu [Konektor plateb Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce) Kromě kroků nastavení eCommerce popsaných v tomto tématu musí být nastaven parametr **Povolit nastavení informací o platbě v elektronickém obchododování** na hodnotu **Pravda** v nastavení konektoru Adyen. 
- **Konfigurace omnikanálových plateb:** V účetním systému přejděte na **Maloobchod a velkoobchod \> Nastavení centrály \> Parametry \> Sdílené parametry velkoobchodu**. Pak na kartě **Omnikanálové platby** nastavte možnost **Použít omnikanálové platby** na **Ano**. Ve verzích Commerce 10.0.12 a novějších je toto nastavení v pracovním prostoru **Správa funkcí**. Vyberte **Omnikanálové platby** a klikněte na **Povolit hned**. 
- **Platební služby:** Kontaktní centrum používá výchozí platební konektor na stránce **Platební služby** ke zpracování plateb. Chcete-li podporovat scénáře jako například "koupit pomocí call centra, vyzvednout v obchodě", musí být tento výchozí konektor platby musí být konektor Adyen platby nebo platební konektor splňující požadavky na implementaci pro platby pomocí Omni kanálu.
- **Služba EFT:** platby prostřednictvím platebního terminálu je nutné nastavit na pevné záložce **Služba EFT** hardwarového profilu. Konektor Adyen podporuje scénáře omnikanálových plateb ihned po vybalení. Ostatní platební konektory, které **podporují** rozhraní iNamedRequestHandler, mohou být použity také v případě, že podporují omnikanálové platby.
- **Dostupnost platebního konektoru**: Pokud je objednávka odvolána, řádky úhrady plateb, které jsou odvolány spolu s objednávkou, obsahují název platebního konektoru, který byl použit k vytvoření autorizací přiřazených k dané objednávce. Po splnění objednávky se sada SDK Platby pokusí použít stejný konektor, který byl použit k vytvoření původního povolení. Proto musí být pro záznam k dispozici platební konektor, který má stejné vlastnosti obchodníka. 
- **Typy karet:** pro správné fungování omni kanálů musí mít každý kanál stejné nastavení pro typy úhrad, které lze použít pro omni kanál. Toto nastavení zahrnuje ID metod plateb a ID typů karet. Pokud má například typ úhrady **Karty** ID **2** v nastavení online obchodu, měl by mít stejné ID v nastavení maloobchodu. Stejný požadavek se vztahuje na ID typů karet. Pokud je číslo karty **12** v online obchodu nastaveno na **VISA**, stejné ID by mělo být nastaveno pro maloobchod. 
- Retail Modern POS pro Windows nebo Android se zabudovanou hardwarovou stanicí   -nebo-
- Modern POS pro iOS nebo Cloud POS s připojenou sdílenou hardwarovou stanicí. 

### <a name="basic-principle-supporting-omni-channel-payments"></a>Základní princip podporující omnikanálové platby

Platební konektory a zpracovatelé plateb používají tokeny nebo odkazy, které odkazují na interakce související s platbami kartou. Je-li například požadováno ověření platby, je k dispozici odkaz na tuto autorizaci. Proto může být autorizace odkazována později při zachycení finančních prostředků v době plnění. Tato autorizace je jedinečná pro obchodníka, platební konektor a procesor. 

Pokud byla objednávka, která byla vytvořena v režimu online, vydána v obchodě, je nutné stornovat a používat stejné platební podrobnosti pro tuto objednávku. Pokud jsou původní podrobnosti poskytnuty jako součást žádosti o zaznamenání platby na původní autorizaci, může zpracovatel platby zpracovat požadavek a zaznamenat platbu. 

Chcete-li správně odkazovat na online objednávku, musí být k dispozici také konektor platby "karta není přítomna", který podporuje stejný procesor. Tímto způsobem může systém POS mít jeden procesor pro platby "kartou", ale může mít také přístup k jiným platebním konektorům, aby mohl vyplnit objednávky vytvořené v jiných kanálech pomocí různých platebních procesorů. 

## <a name="supported-scenarios"></a>Podporované scénáře

Podporovány jsou následující scénáře omnikanálových plateb:

- Nákup online, vyzvednutí v obchodě
- Nákup v kontaktním středisku a vyzvednutí v obchodě
- Nákup v obchodě A, vyzvednutí v obchodě B
- Nákup v obchodě A, odeslání zákazníkovi

    > [!NOTE]
    > Platby provedené v call centru, které se mapují na platební funkci „Normální“, musí být označeny jako **Zaplatit předem** = **Ano**, aby se promítly do splatné částky při odvolání objednávky v POS. Platby nezaplacené předem typu „Normální“ nebudou při odvolání objednávky v POS rozpoznány. 

Jsou podporovány i varianty těchto scénářů. Například online objednávka může obsahovat jak řádky, které budou expedovány zákazníkovi, tak řádky, které budou v obchodě vydány. Všechny možnosti plnění objednávky jsou podporovány prostřednictvím omnikanálových plateb. 

V následujících oddílech jsou popsány kroky pro jednotlivé scénáře a ukazují, jak spustit scénář pomocí ukázkových dat. 

### <a name="buy-online-pick-up-in-store"></a>Nákup online, vyzvednutí v obchodě

Než začnete, musíte se ujistit, že jsou splněny následující předpoklady:

- Máte referenční výkladní skříň, kde je konfigurován konektor Adyen.
- Možnost **Omnikanálové platby** na stránce **Sdílené parametry velkoobchodu** je nastavená na **Pravda**. V novějších verzích je toto nastavení přesunuto do pracovního prostoru **Správa funkcí**, kde si můžete vybrat funkci **Omnikanálové platby** a kliknout na **Povolit hned**. 
- Platební konektor Adyen je nakonfigurován pro registrační pokladnu Houston POS.
- Retail Modern POS pro Windows nebo Android se zabudovanou hardwarovou stanicí   -nebo-
- Modern POS pro iOS nebo Cloud POS s připojenou sdílenou hardwarovou stanicí. 

Pokud chcete spustit tento scénář, postupujte takto:

1. V referenční výkladní skříni vytvořte objednávku pro výdej v obchodě. Je nutné vybrat obchod **Houston**. 
2. Projděte kroky odbavení a zaplaťte pomocí čísla testovací kreditní karty. Čísla testovacích kreditních karet lze nalézt na stránce [Stránka s čísly testovacích karet Adyen](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description).
3. Ve velkoobchodu použijte dávkovou úlohu **synchronizovat objednávky** a distribuční plán **P-001** k vytvoření objednávek v kanceláři.
4. V POS na úvodní stránce vyberte operaci **Objednávky k výdeji** a zobrazte objednávky pro výdej v obchodě. 
5. Vyberte jeden nebo více řádků z objednávky, která byla vytvořena v referenčním výkladní skříni, a poté vyberte **vyzvednout**.

    Objednávka se načte z kanceláře. 

6. Když jsou podrobnosti řádku objednávky načteny z kanceláře a je zjištěna platba kartou, kterou lze použít pro omni kanál, bude informována o tom, že je k dispozici způsob platby.
7. Vyberte **Použít dostupný způsob platby** k dokončení transakce pomocí podrobností o kartě, které byly zadány v referenční výkladní skříni.

    Řádky objednávky jsou načteny na stránce transakce a splatný zůstatek je 0 (nula). 

8. Pokud chcete zobrazit řádek úhrady získaný z online objednávky, vyberte kartu **Platby**. 
9. Chcete-li transakci dokončit, vyberte některý způsob platby. 

### <a name="buy-in-call-center-pick-up-in-store"></a>Nákup v kontaktním středisku a vyzvednutí v obchodě

1. V aplikaci Commerce na stránce **Sužby pro zákazníky** zadejte do vyhledávacího pole text **Karen Berg** a vyberte **Hledat.** 
3. Ve výsledcích hledání vyberte položku **Karen Berg**.
4. Po načtení Karen na stránku **Služby pro zákazníky** vyberte možnost **Nová prodejní objednávka.**
5. Na stránce Nová prodejní objednávka vyberte **Záhlaví**, aby se zobrazilo záhlaví objednávky. 
6. Na stránce **Záhlaví** objednávky nastavte web na **Centrální** a sklad na **Houston**.
7. Na kartě **Dodávka** nastavte pole **Způsob dodání** na **60** pro vyzvednutí zákazníkem.
8. Vyberte **Řádky** a poté přidejte do objednávky jeden nebo více řádků. 
9. Výběrem možnosti **Dokončit** zadejte tok dokončení objednávky.
10. Přejděte do části platby, vyberte **Přidat** a poté vyberte řádek, na kterém je typ způsobu platby nastaven na možnost **Karty.** 
11. Výběrem znaménka plus (**+**) přidejte platbu kartou. 
12. Zadejte podrobnosti o čísle zkušební kreditní karty, které jste našli na [stránce Čísla zkušební karty Adyen](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description) a potom vyberte **OK**.

    > [!NOTE]
    > Pokud se značka karty pro zadané číslo karty odlišuje od značky, která byla vybrána při zahájení platby, platba přesto projde. Bude však zaúčtována na účty, které jsou mapovány na značku karty vybrané v kroku 10.

12. Znovu klikněte na **OK** k zavření dialogového okna **Platby dokončení objednávky**.
13. Na stránce **Souhrn prodejní objednávky** vyberte možnost **Odeslat**.
14. V POS na úvodní stránce vyberte operaci **Objednávky k výdeji** a zobrazte objednávky pro výdej v obchodě. 
15. Vyberte jeden nebo více řádků z objednávky, která byla vytvořena v referenčním výkladní skříni, a poté vyberte **vyzvednout**.

    Objednávka se načte z kanceláře. 

16. Když jsou podrobnosti řádku objednávky načteny z kanceláře a je zjištěna platba kartou, kterou lze použít pro omni kanál, bude informována o tom, že je k dispozici způsob platby.
17. Vyberte **Použít dostupný způsob platby** k dokončení transakce pomocí podrobností o kartě, které byly zadány v referenční výkladní skříni.

    Řádky objednávky jsou načteny na stránce transakce a splatný zůstatek je 0 (nula).

18. Pokud chcete zobrazit řádek úhrady získaný z online objednávky, vyberte kartu **Platby**. 
19. Chcete-li transakci dokončit, vyberte některý způsob platby. 

### <a name="buy-in-store-a-pick-up-in-store-b"></a>Nákup v obchodě A, vyzvednutí v obchodě B

1. Spusťte POS pro obchod Houston.
2. Na stránce **Transakce** přidejte do transakce Karen Berg pomocí číselného panelu a zadejte **2001.**
3. Přidejte do transakce jeden nebo více řádků.
4. Pokud chcete zobrazit možnosti objednávky, vyberte **Objednávky**.
5. Vyberte **Vyzvednout vše** a až budete vyzváni, vyberte volbu **Objednávka zákazníka**.
6. Do vyhledávacího panelu zadejte **Seattle** a pak vyberte obchod v **Seattlu** pro výdej. 
7. Kliknutím na **OK** přijměte aktuální datum jako datum výdeje.
9. Vyberte **Platba kartou** pro zahájení platby.
10. Uhraďte kartou částku, která je splatná jako záloha. 
11. Dokončete zálohovou platbu na platebním terminálu. 
12. Po zaplacení vkladu vyberte možnost pro použití stejné karty pro plnění a čekání na dokončení objednávky. 
13. Spusťte POS pro obchod Seattle.
14. V POS na úvodní stránce vyberte operaci **Objednávky k výdeji** a zobrazte objednávky pro výdej v obchodě. 
15. Vyberte jeden nebo více řádků z objednávky, která byla vytvořena v referenčním výkladní skříni, a poté vyberte **vyzvednout**.

    Objednávka se načte z kanceláře. 

16. Když jsou podrobnosti řádku objednávky načteny z kanceláře a je zjištěna platba kartou, kterou lze použít pro omni kanál, bude informována o tom, že je k dispozici způsob platby.
17. Vyberte **Použít dostupný způsob platby** k dokončení transakce pomocí podrobností o kartě, které byly zadány v referenční výkladní skříni.

    Řádky objednávky jsou načteny na stránce transakce a splatný zůstatek je 0 (nula).

18. Pokud chcete zobrazit řádek úhrady získaný z online objednávky, vyberte kartu **Platby**. 
19. Chcete-li transakci dokončit, vyberte některý způsob platby. 

### <a name="buy-in-store-a-ship-to-customer"></a>Nákup v obchodě A, odeslání zákazníkovi

1. Spusťte POS pro obchod Houston.
2. Na stránce **Transakce** přidejte do transakce Karen Berg pomocí číselného panelu a zadejte **2001.**
3. Přidejte do transakce jeden nebo více řádků.
4. Pokud chcete zobrazit možnosti objednávky, vyberte **Objednávky**.
5. Vyberte **Odeslat vše** a až budete vyzváni, vyberte volbu **Objednávka zákazníka**.
6. Na stránce způsobu dopravy vyberte **Standardní přes noc** a potom vyberte **OK** přijmout dnešní datum jako datum odeslání. 
7. Kliknutím na **OK** přijměte aktuální datum jako datum výdeje.
8. Vyberte **Platba kartou** pro zahájení platby.
9. Uhraďte kartou částku, která je splatná jako záloha. 
10. Dokončete zálohovou platbu na platebním terminálu. 
11. Po zaplacení vkladu vyberte možnost pro použití stejné karty pro plnění a čekání na dokončení objednávky.

Pokud je objednávka vyzvednuta, zabalena a fakturována v kanceláři, budou se údaje o platbě poskytované v POS používat k zaznamenání finančních prostředků pro zboží, které je dodáno zákazníkovi. 

## <a name="scenario-details"></a>Podrobnosti scénáře

Kromě základních scénářů, které byly právě popsány, bylo v sadě SDK plateb provedeno několik vylepšení pro podporu omnikanálových plateb. 

### <a name="pos"></a>POS

#### <a name="single-swipedip-for-customer-orders"></a>Jedno protažení/přiložení pro objednávky zákazníka

Před implementací funkce omnikanálových plateb to bývalo tak, že při vytvoření objednávek zákazníka, které obsahovaly zálohu, V POS, museli zákazníci protáhnout (nebo přiložit) kartu dvakrát: jednou pro zaplacení zálohy a podruhé k tokenizaci karty pro následné plnění objednávky. Po zapnutí funkce tokenizace omnikanálu musí zákazníci protáhnout kartu jenom jednou, aby zaplatili zálohu a autorizovali částku za zboží, které bude dodáno později. V okamžiku plnění jsou zachyceny autorizované finance. Před implementací funkce omnikanálové tokenizace byl vytvořen pouze opakovaný token karty pro následné plnění objednávky. Proto nebyly finanční prostředky pro nevyřízené plnění autorizovány a protože tyto finance nebyly pro tento konkrétní nákup blokovány, bylo méně pravděpodobné, že by mohly být zachyceny později.

> [!NOTE]
> Aplikace Retail verze 8.1.3 nepodporuje jedno protažení. Objednávky zákazníka ve verzi 8.1.3 používají stejný tok, který byl použit před implementací funkce tokenizace omnikanálu. 

### <a name="cards-that-cant-issue-recurring-card-tokens"></a>Karty, které nemohou vydávat opakované tokeny karet

Některé karty nelze použít pro omnikanálové platby, protože nepodporují vydávání opakovaných tokenů karet. Když je v POS vytvořena objednávka a záloha je zaplacena pomocí karty, která nepodporuje tokeny opakovaných karet, použije se předchozí tok tokenu karty. Proto musí mít zákazník, který chce poskytnout platbu, která bude použita pro následné plnění objednávky, k dispozici druhou kartu. Pokud druhá karta nepodporuje opakované tokeny karet, bude akce tokenizace odmítnuta a pokladník bude vyzván, aby požádal zákazníka o poskytnutí druhé karty. 

### <a name="using-a-different-card"></a>Použití jiné karty

Zákazník, který přichází do obchodu vyzvednout objednávku, má možnost použít jinou kartu. Když pokladník obdrží výzvu k **použití dostupného způsobu platby** v době výdeje objednávky, může se zeptat, zda chce zákazník používat stejnou kartu. Pokud zákazník ztratil kartu, která byla použita při vytvoření objednávky, a chce zaplatit objednávku pomocí jiné karty, může pokladník vybrat možnost **Použít jiný způsob platby**. Pokud se zákazník později pokusí vyzvednout další zboží ze stejné objednávky a platí autorizace původní karty, může se pokladník znovu zeptat, zda chce zákazník použít tuto kartu.

### <a name="invalid-authorizations"></a>Neplatné autorizace

Pokud karta, která byla použita k vytvoření objednávky, již není platná, požadavek na zachycení platby se při výběru produktů nezdaří. Konektor platby POS se pak pokusí vytvořit novou autorizaci a zachycení pomocí stejných podrobností o kartě. Pokud se nové povolení nebo zachycení nezdaří, pokladník bude informován o tom, že platbu nelze zpracovat. Pokladník poté musí od zákazníka získat novou platbu. 

### <a name="multiple-available-payments"></a>Více dostupných plateb

Když má objednávka více nabídek a je vybráno více řádků, pokladník nejprve obdrží výzvu **Použít dostupný způsob platby**. Pokud existuje více karet, když pokladník vybere možnost **Použít dostupný způsob platby**, budou zachyceny existují řádky výběru platby, dokud nebude splněn zůstatek u aktuálně vybíraného zboží. Pokladník nebude mít možnost vybrat kartu, která má být použita pro vybírané zboží. 

## <a name="related-topics"></a>Související témata

- [Časté dotazy k platbám](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [Platební konektor Dynamics 365 pro Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
- [Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce](https://docs.microsoft.com/dynamics365/commerce/cpe-bopis)



[!INCLUDE[footer-include](../includes/footer-banner.md)]