---
title: Vytvoření vrácení v POS
description: Tento článek popisuje, jak iniciovat vrácení u transakcí typu cash and carry nebo objednávek zákazníků v aplikaci Microsoft Dynamics 365 Commerce Point of Sale (POS).
author: hhainesms
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: a49e9abd0143d480cc1cafb05be5e995fb3cebdd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856991"
---
# <a name="create-returns-in-pos"></a>Vytvoření vrácení v POS

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak iniciovat vrácení u transakcí typu cash and carry nebo objednávek zákazníků v aplikaci Microsoft Dynamics 365 Commerce Point of Sale (POS).

> [!NOTE]
> Ve verzi Commerce verze 10.0.20 a novějších je k dispozici nová funkce s názvem **Sjednocené prostředí pro zpracování vrácení v POS**. Tato funkce poskytuje více konsistentní a jednotnější proces vrácení v POS, bez ohledu na typ transakce (typu cash and carry nebo objednávky zákazníka) nebo původní kanál, ve kterém byla objednávka vytvořena. Doporučujeme, aby všechny organizace zapnuly tuto novou funkci, které pomůže zlepšit celkovou spolehlivost zpracování vratek prostřednictvím POS.
>
> Poté, co funkci zapnete, ji nelze vypnout.

## <a name="process-returns-by-using-the-return-transaction-operation"></a>Zpracování vratek pomocí operace vrácení transakce

Doporučujeme přidat operaci transakce vrácení do svého [rozložení obrazovky POS](pos-screen-layouts.md). Ve verzích starších než Commerce 10.0.20 operace vrácení transakce správně podporuje zpracování vratek pouze u transakcí typu cash and carry. Po zapnutí funkce **Sjednocené prostředí pro zpracování vrácení v POS** v Commerce 10.0.20 nebo novější verzi již operace vrácení transakce také podporuje zpracování vratek, která pocházejí z objednávek zákazníků, jako jsou objednávky typu „vyzvednutí“ nebo „odeslání domů“, které jsou již fakturovány.

Z operace transakce vrácení mohou uživatelé vyhledávat transakce typu cash and carry nebo objednávku zákazníka, která se má vrátit, zadáním některého z následujících čtyř vyhledávacích kritérií. Uživatelé mohou tato kritéria zadat pomocí klávesnice zařízení, klávesnice na obrazovce nebo čtečky čárových kódů.

- ID účtenky
- Číslo objednávky
- ID odkazu na kanál (známé také jako ID potvrzení objednávky)
- ID faktury

Pokud je nalezena transakce nebo objednávka, která odpovídá kritériím vyhledávání, zobrazí se stránka **Vratné produkty**. Zde mohou uživatelé určit položky, které se vracejí. Mohou také zadat vrácené množství a kódy důvodu.

U každého řádku objednávky v seznamu vratných produktů POS zobrazuje informace o původním množství nákupu a množstvích z jakýchkoli vrácených položek, které byly dříve zpracovány. Vrácené množství, které uživatel zadá pro řádek objednávky, musí být menší nebo rovné hodnotě pole **Dostupné k vrácení**.

![Stránka vratných produktů.](media/returnslist.png)

Pokud má uživatel během zpracování vratky fyzický produkt a tento produkt má čárový kód, může uživatel naskenováním čárového kódu zaregistrovat vrácení. Každé naskenování čárového kódu zvyšuje vrácené množství o jednu položku. Pokud však štítek s čárovým kódem obsahuje vložené množství, bude toto množství zadáno do pole **Nyní se vrací**.

Uživatelé mohou také na stránce **Vratné výrobky** ručně vybrat položky, které se vrátí, a poté aktualizovat pole **Nyní se vrací** pomocí podokna podrobností napravo.

Pokud je pro transakci určeno maximální dostupné množství **Nyní se vrací**, uživatel může vybrat v pruhu aplikace POS operaci **Vybrat vše** a nastavit tak maximální vratné množství na všech řádcích.

Pro každý řádek, který má množství **Nyní se vrací**, musí uživatel vybrat kód důvodu vrácení v panelu podrobností. U vratek transakcí cash and carry jsou kódy důvodů vrácení konfigurovány jako informační kódy v profilu funkce obchodu. U vratek objednávek zákazníků jsou kódy důvodů vrácení konfigurovány na stránce **Kódy důvodů vrácení** v centrále Dynamics 365 Commerce.

Po nastavení vráceného množství a kódu důvodu pro každou položku, která musí být vrácena, může uživatel vybrat v pruhu aplikace POS operaci **Vrátit** a pokračovat ve zpracování. Zobrazí se stránka transakce POS, kde byly do košíku přidány vratné položky vybrané na předchozí stránce. Množství **Nyní se vrací** pro položky se v transakci zobrazí jako řádky se záporným množstvím a vypočítá se celková refundace.

Uživatelé mohou k transakci vrácení přidat řádky, pokud vytvářejí objednávku směny. Uživatelé mohou také do transakce vrácení přidat více ad-hoc vrácených položek pomocí operace **Vrátit produkt** pro vybraný prodejní řádek s kladným množstvím, který byl přidán.

> [!NOTE]
> Operace **Vrátit produkt** v POS neposkytuje žádné ověření vůči jakékoli původní transakci a umožňuje vrácení jakéhokoli produktu. Proto doporučujeme, aby tuto operaci mohli provádět pouze oprávnění uživatelé, nebo aby bylo při této operaci vyžadováno přepsání správce.

Pokud je refundace splatná při placení, mohou organizace konfigurovat [zásady vracení plateb](refund_policy_returns.md), které omezují platební metody, jež lze použít k vrácení peněz zákazníkům. Pokud byla původní transakce zaplacena kreditní kartou, uživatelé mohou mít v závislosti na procesoru plateb a konfiguraci systému možnost [vrátit peníze na původní kartu](dev-itpro/linked-refunds.md). V takovém případě lze refundaci zpracovat, aniž by bylo nutné, aby zákazník znovu přejel kreditní kartou čtečku. K vrácení peněz se používá token původní platby.

## <a name="other-return-options-in-pos"></a>Další možnosti vrácení v POS

Když je zapnuta funkce **Sjednocené prostředí pro zpracování vrácení v POS**, mohou uživatelé také používat operaci **Zobrazit deník** v POS k zahájení vrácení transakce typu cash and carry nebo objednávky zákazníka. Poté mohou vybrat transakci v deníku a následně zvolit operaci **Vrátit** v pruhu aplikace POS. Tato operace je k dispozici, pouze pokud jsou na objednávce vratné řádky. Iniciuje stejné uživatelské prostředí jako operace **Vrátit transakci**.

Uživatelé mohou také použít operaci **Odvolat objednávku** v POS k vyhledávání a odvolání objednávek zákazníků. (Tuto operaci nelze použít pro transakce cash and carry). V tomto případě lze po výběru objednávky zákazníka použít operaci **Vrátit** v pruhu aplikace POS k zahájení vrácení objednávky zákazníka. Tato operace je k dispozici, pouze pokud jsou na objednávce vratné řádky. Iniciuje stejné uživatelské prostředí jako operace **Vrátit transakci** nebo **Zobrazit deník**.

## <a name="return-orders-are-posted-to-commerce-headquarters-as-sales-orders"></a>Vrácené objednávky se zaúčtují do centrály Commerce jako prodejní objednávky 

Když je zapnuta funkce **Sjednocené prostředí pro zpracování vrácení v POS**, všechny vrácené položky vytvořené v POS se zapisují do centrály Commerce jako prodejní objednávky se zápornými řádky. Ve verzích starších než Commerce 10.0.20 si uživatelé mohou vybrat, zda mají být vrácené objednávky zaúčtovány jako prodejní objednávky se zápornými řádky, nebo zda to mají být vrácené objednávky, které jsou vytvořeny prostřednictvím procesu autorizace vrácení zboží (RMA). 

Ve funkci **Sjednocené prostředí pro zpracování vrácení v POS** byla možnost použít proces RMA k vytvoření vratek v POS označena jako zastaralá. Po zapnutí této funkce budou všechny vrácené položky vytvořeny jako prodejní objednávky se zápornými řádky.

## <a name="offline-return-processing-improvements"></a>Vylepšení v oblasti offline zpracování vratek

Ve většině případů, když je vrácení zpracováno v POS, se systém pokusí uskutečnit volání služby v reálném čase (RTS) do centrály Commerce, aby ověřil aktuální množství, která jsou k dispozici k vrácení. Toto ověření pomáhá předcházet podvodným scénářům, kdy se zákazník pokusí vrátit stejnou položku na více místech.

Abychom zvládli situace, kdy volání RTS nelze provést z důvodu problémů se sítí nebo připojením, byl zaveden proces periodické synchronizace dat o vráceném množství z centrály Commerce do databáze kanálu obchodu. Toto sledování vratek na straně kanálu pomáhá zajistit, aby množství **Dostupné k vrácení** zobrazená v POS byla přiměřeně přesná, i když je POS ve stavu offline. Zajišťuje také, že POS může i nadále ověřovat informace na straně kanálu, aby se zabránilo podvodným vrácením.

Aby bylo možné vhodným způsobem použít proces vrácení offline, měly by organizace naplánovat v centrále Commerce dávkovou úlohu **Aktualizovat vrácené množství**, aby byla často spouštěna. Doporučujeme, aby tato úloha probíhala ve stejné frekvenci jako úloha P, která stahuje nové transakce z kanálů Commerce do centrály Commerce.

Úloha **Aktualizovat vrácené množství** vypočítá množství, které je k dispozici pro vrácení u všech prodejních objednávek, které se nacházejí v centrále Commerce. Data, která úloha vypočítá, musí být poté odeslána do databází kanálů, aby bylo možné aktualizovat kanály úložiště. K tomuto účelu se používá distribuční úloha **Vrácené množství** (1200). Protože data o vratném množství jsou synchronizována z centrály Commerce, může POS použít informace o vrácení na straně kanálu k ověření množství **Dostupné k vrácení** pro daný řádek prodeje, je-li vrácení zpracováno v POS, ale nelze provést volání RTS.

Když nelze uskutečnit volání RTS a POS používá pro ověření vratky data na straně kanálu, varovná zpráva informuje uživatele, že vytvářejí „offline“ vratku. Proto uživatelé vědí, že množství **Dostupné k vrácení**, které se zobrazuje v POS, může být zastaralé a nadále nepřesné, v závislosti na tom, kdy byla naposledy zpracována úloha **Aktualizovat vrácené množství** a synchronizována s kanálem.

Například zákazník nedávno zpracoval vratku pro řádek objednávky v jiném kanálu, ale tato data ještě nebyla synchronizována s databázemi kanálu prostřednictvím úlohy **Aktualizovat vrácené množství**. Zákazník poté přejde do jiného obchodu a pokusí se vrátit stejnou položku znovu. V tomto případě, pokud obchod nemůže provést volání RTS do centrály Commerce, aby získal data o vrácení v reálném čase, POS umožní položku vrátit znovu. Uživatel je však varován, že informace, které se používají k ověření vrácení, mohou být zastaralé. Zpráva, kterou uživatel obdrží, je pouze varovnou zprávou. Nebrání uživateli pokračovat ve zpracování vratky.

Pokud informace na straně kanálu nejsou z nějakého důvodu aktuální a je zpracováno offline vrácení pro množství, které přesahuje skutečné množství **Dostupné k vrácení**, při spuštění zaúčtování příkazu pro vytvoření transakce v centrále Commerce může dojít k chybě.

> [!NOTE]
> Když je zapnuta funkce **Sjednocené prostředí pro zpracování vrácení v POS**, jsou k dispozici nové volitelné funkce, které podporují ověřování vrácení serializovaného produktu. Další informace viz [Vrácení produktů řízených sériovým číslem v aplikaci Point of Sale (POS)](POS-serial-returns.md).

## <a name="version-details"></a>Podrobnosti verze

Následující seznam uvádí minimální požadavky na verzi pro různé součásti.
- Ústředí Commerce: verze 10.0.20
- Commerce Scale Unit (CSU): verze 9.30
- Pokladní místo (POS): verze 9.30

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Povolení správného výpočtu daně pro vrácení s částečným množstvím

Tato funkce zajišťuje, že při vrácení objednávky s použitím více faktur se daně nakonec budou rovnat původně účtované částce daně.

1. V pracovním prostoru **Správa funkcí** vyhledejte možnost **Povolení správného výpočtu daně pro vrácení s částečným množstvím**.
1. Vyberte funkci **Povolení správného výpočtu daně pro vrácení s částečným množstvím** a poté vyberte **Povolit**.

## <a name="set-up-return-locations-for-retail-stores"></a>Nastavení skladových umístění vratek v maloobchodech

Commerce vám umožní nastavit skladová umístění vratek, která jsou založena na maloobchodních informačních kódech a kódech důvodu z oblasti prodeje a marketingu. Pokladníci často udávají důvod vrácení nákupu zákazníkem. Můžete určit, že vrácené produkty budou přiřazeny do různých míst pro vrácení ve skladu, v závislosti na odpovědi pokladníka na informační kódy a kódy důvodu, které pokladníci vyberou v pokladně.

Zákazník například vrátí vadný produkt a pokladní zpracuje transakci vrácení. Když Retail POS zobrazí informační kód pro vratky, pokladník vybere dílčí kód pro vadné vratky. Vrácený produkt je pak automaticky přiřazen ke konkrétnímu místu vrácení.

Místo pro vrácení může být obchod, sklad, umístění v obchodě nebo skladu nebo dokonce konkrétní paleta, v závislosti na skladových místech, která vaše organizace nastavila. Každé místo pro vrácení lze mapovat na jeden nebo více maloobchodních informačních kódů a kódů důvodu prodeje a marketingu.

### <a name="prerequisites"></a>Předpoklady

Dříve než lze vytvořit skladová místa pro vratky, je nutné nastavit následující prvky:

- **Maloobchodní informační kódy** – výzvy v pokladně POS, které jsou nastaveny v modulu **Maloobchod**. Další informace naleznete v tématu [Nastavení informačních kódů](/dynamicsax-2012/appuser-itpro/setting-up-info-codes).
- **Kódy důvodu pro prodej a marketing** – výzvy v pokladně POS, které jsou nastaveny v modulu **Prodej a marketing**. Další informace naleznete v tématu [Nastavení kódů důvodu](/dynamicsax-2012/appuser-itpro/set-up-return-reason-codes).
- **Skladová místa** – místa, ve kterých jsou ukládány zásoby. Další informace viz téma [Nastavení skladových míst](/dynamicsax-2012/appuser-itpro/about-locations).
    
### <a name="set-up-return-locations"></a>Nastavení skladových umístění vratek

Chcete-li nastavit skladová místa pro vratky, postupujte následujícím způsobem.

1. Přejděte do nabídky **Maloobchod a obchod \> Nastavení kanálu \> Sklady** a vyberte sklad.
1. Na záložce **Maloobchod** vyberte v poli **Výchozí místo pro vrácení** skladové místo, které chcete použít pro vrácení, kde informační kódy nebo kódy důvodu nejsou namapovány na místa vrácení.
1. V poli **Výchozí vrácená paleta** vyberte paletu, které chcete použít pro vrácení, kde informační kódy nebo kódy důvodu nejsou namapovány na místa vrácení.
1. Přejděte na **Maloobchod a obchod \> Řízení zásob \> Místa vratek**.
1. Vyberte **Nová**, chcete-li vytvořit novou zásadu umístění pro vrácení.
1. Zadejte jedinečný název a popis skladového místa pro vratky.

    > [!NOTE]
    > Název je zadán automaticky, je-li nastavena číselná řada pro skladová umístění vratek.

1. Na záložce **Všeobecné** nastavte možnost **Tisk štítků** na **Ano**, aby se tiskly štítky pro všechny produkty, které jsou přiřazeny k místům vrácení.
1. Nastavte možnost **Blokovat zásoby** na **Ano**, chcete-li přijmout vrácené produkty do výchozího místa mimo sklad a zabránit jeho prodeji.
1. Chcete-li namapovat konkrétní maloobchodní informační kódy a dílčí kódy na místa vrácení, postupujte takto:

    1. Na pevné záložce **Maloobchodní informační kódy** vyberte **Přidat**.
    1. V poli **Informační kód** vyberte informační kód pro vratky.
    1. V poli **Dílčí kód** vyberte dílčí kód důvodu vrácení. Pole **Popis** ukazuje popis vybraného dílčího kódu.
    1. V poli **Obchod** vyberte skladové místo, kde chcete použít informační kód.
    1. K určení místa vrácení použijte pole **Sklad**, **Umístění** a **ID palety**. Například pro výběr místa v obchodě vyberte obchod v poli **Obchod** a umístění v poli **Umístění**.
    1. Zapnutím políčka **Blokovat zásoby** vyberete vrácené produkty ze zásob a zabráníte jejich prodeji.

1. Chcete-li namapovat konkrétní prodejní a marketingové kódy důvodu na místa vrácení, postupujte takto:

    1. Na záložce **Kódy prodejních a marketingových důvodů** vyberte **Přidat**.
    1. Poté v poli **Kód důvodu** vyberte nový kód důvodu pro vratky. Pole **Popis** ukazuje popis vybraného kódu důvodu.
    1. V poli **Obchod** vyberte skladové místo, kde chcete použít kód důvodu.
    1. K určení místa vrácení použijte pole **Sklad**, **Umístění** a **ID palety**. Pokud chcete například určit paletu v umístění ve skladu, vyberte sklad v poli **Sklad**, místo v poli **Umístění** a paletu v poli **ID palety**.
    1. Zapnutím políčka **Blokovat zásoby** vyberete vrácené produkty ze zásob a zabráníte jejich prodeji.

    > [!NOTE]
    > Pokud se pro položku použije zásada místa vrácení, ale důvod vrácení vybraný pokladníkem neodpovídá žádnému kódu uvedenému na záložce **Maloobchodní informační kódy** nebo **Kódy prodejních a marketingových důvodů**, je položka odeslána do výchozího místa vrácení, které je definováno na stránce **Sklad**. Kromě toho nastavení zaškrtávacího políčka **Blokovat zásoby** na záložce **Všeobecné** ve stránce **Místa vrácení** určuje, zda má být vrácená položka blokována jako zásoba.

1. Přejděte na **Maloobchod a obchod \> Hierarchie obchodních produktů**.
1. Na záložce **Spravovat vlastnosti kategorie zásob** vyberte v poli **Místo vratky** místo vrácení. Protože pro stejný obchod lze definovat více zásad místa vrácení, hodnota, kterou zde vyberete, určuje použitou zásadu místa vrácení.

## <a name="additional-resources"></a>Další prostředky

[Vrácení produktů řízených sériovým číslem v aplikaci Point of Sale (POS)](POS-serial-returns.md)

[Propojené refundace dříve schválených a potvrzených transakcí](dev-itpro/linked-refunds.md)

[Vytvoření a aktualizace zásady vrácení a refundace pro kanál](refund_policy_returns.md)

[Vizuální konfigurace uživatelského rozhraní POS](pos-screen-layouts.md)
