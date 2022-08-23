---
title: Nakonfigurujte způsob platby zákaznického účtu pro stránky elektronického obchodování B2B
description: Tento článek popisuje, jak nakonfigurovat způsob platby zákaznického účtu v Microsoft Dynamics 365 Commerce. Popisuje také, jak úvěrové limity ovlivňují zachycení platby na účet na webech elektronického obchodování mezi podniky (B2B).
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: b8424920c3a177e01b71fc1c288b7acdd97ef191
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272010"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Nakonfigurujte způsob platby zákaznického účtu pro stránky elektronického obchodování B2B

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak nakonfigurovat způsob platby zákaznického účtu v Microsoft Dynamics 365 Commerce. Popisuje také, jak úvěrové limity ovlivňují zachycení platby na účet na webech elektronického obchodování mezi podniky (B2B).

Maloobchodní prodejci mohou přijímat různé typy plateb za výrobky a služby, které prodávají v kanálu elektronického obchodování. Každý typ platby, kterou prodejce přijímá, musí být nakonfigurován při nastavení systému v aplikaci Dynamics 365 Commerce. Platební metoda zákaznického účtu (nebo „na účet“) musí být podporována na webech B2B elektronického obchodování. 

## <a name="prerequisites"></a>Předpoklady

1. Přidejte platební metodu zákaznického účtu v centrále Commerce.
2. Přiřaďte platební metodu zákaznického účtu ke kanálu elektronického obchodování.
3. Ujistěte se, že je pro zákazníka povolena vlastnost **Povolit na účet** v nabídce **Maloobchod a velkoobchod \> Zákazníci \> Všichni zákazníci \> Výchozí nastavení plateb** v centrále Commerce.

    > [!NOTE]
    > Pokud mají mít všichni zákazníci povolenu platební metodu na účet, nastavte vlastnost **Povolit na účet** na **Ano** pro výchozího zákazníka kanálu, který je přidružen k webu B2B. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Povolte způsob platby zákaznického účtu v konfigurátoru webů Commerce 

Chcete-li povolit způsob platby zákaznického účtu v konfigurátoru webů Commerce, postupujte takto.

1. Přejděte na **Nastavení webu \> Rozšíření**.
1. Nastavte vlastnost **Povolit platby na zákaznický účet** na **Povoleno pro zákazníky B2B**. 
1. Vyberte možnost **Uložit a publikovat**.

> [!NOTE]
> Nové nastavení webu se projeví až po aktualizaci souboru app.settings.json. Další informace viz [Aktualizace knihoven SDK a modulů](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Povolte platební metodu zákaznického účtu na stránce pokladny pro web elektronického obchodování B2B

Chcete-li povolit platební metodu zákaznického účtu na stránce pokladny pro web elektronického obchodování B2B, postupujte takto.

1. V konfigurátoru webů Commerce vyhledejte a upravte stránku pokladny nebo fragment, který obsahuje modul pokladny pro web elektronického obchodování B2B.
1. Ve slotu **Kontejner sekce pokladny** vyberte **Přidat modul** a pak přidejte modul **Platba na účet zákazníka**.
1. Umístěte modul **Platba na účet zákazníka** výběrem třech teček (**...**) a poté vyberte **Posunout nahoru** nebo **Posunout dolů** podle potřeby.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Potvrďte, že byla povolena a zveřejněna platební metoda zákaznického účtu

Chcete-li potvrdit, že byla povolena a zveřejněna platební metoda zákaznického účtu, postupujte takto.

1. Přihlaste se do webu elektronického obchodování.
1. Přidejte produkt do košíku.
1. Přejděte na stránku pokladny. Měli byste vidět novou platební metodu **Zákaznický účet**.

## <a name="work-with-credit-limits"></a>Práce s úvěrovými limity

Když jsou na webu B2B povoleny platby pomocí zákaznických účtů, organizace obvykle chtějí během procesu zachycení objednávky zobrazit informace o úvěrových limitech a zůstatcích těchto limitů. Úvěrový limit pro zákazníka je definován vlastností **Úvěrový limit** na záložce **Úvěry a inkasa** záznamu zákazníka v centrále Commerce. Ve scénářích B2B by však objednávka, kterou zákazník zadá, měla být často fakturována na účet organizace, do které zákazník patří. Proto musíte nastavit vlastnost **Účet faktury** na záložce **Faktura a doručení** záznamu zákazníka na ID zákaznického účtu organizace. Když poté zákazník zadá objednávku na webu B2B, bude objednávka fakturována organizaci. Web B2B bude také používat úvěrový limit organizace namísto limitu definovaného v záznamu zákazníka.

Výpočet a zůstatek úvěrového limitu, které se zobrazují na B2B webu, závisejí na nastavení vlastnosti **Typ úvěrového limitu** v centrále Commerce. Umístění této vlastnosti se liší v závislosti na tom, zda je povolena funkce **Správa úvěrů** v pracovním prostoru **Správa funkcí**:

- Pokud je funkce **Správa úvěrů** povolena, vlastnost se nachází na záložce **Úvěrové limity** v nabídce **Úvěry a inkasa \> Nastavení \> Parametry úvěru a inkasa \> Úvěr**. 
- Pokud je funkce **Správa úvěrů** deaktivována, vlastnost se nachází v části **Třída úvěruschopnosti** v nabídce **Pohledávky \> Nastavení \> Parametry pohledávek \> Třída úvěruschopnosti**.

Vlastnost **Typ úvěrového limitu** má hodnoty **Žádný**, **Zůstatek**, **Zůstatek + dodací list nebo příjemka produktu** a **Zůstatek + vše**. Další informace o těchto hodnotách najdete v tématu [Hodnoty typu úvěrového limitu](/dynamics365/supply-chain/sales-marketing/credit-limits-customers).

> [!NOTE]
> Doporučujeme nastavit vlastnost **Typ úvěrového limitu** na hodnotu **Zůstatek + dodací list nebo příjemka produktu**, aby otevřené prodejní objednávky nepřispívaly k výpočtu zůstatku. Pokud pak vaši zákazníci zadají budoucí objednávky, nemusejí se bát, že tyto objednávky ovlivní jejich aktuální zůstatek.

Další vlastností, která ovlivňuje objednávání na účet, je **Povinný úvěrový limit**, který se nachází na záložce **Úvěry a inkasa** záznamu zákazníka. Nastavením této vlastnosti na **Ano** u konkrétních zákazníků můžete donutit systém, aby zkontroloval jejich úvěrový limit, i když vlastnost **Typ úvěrového limitu** byla nastavena na **Žádný**, aby úvěrový limit nebyl kontrolován u žádného zákazníka.

V současné době nemůže zákazník využívající platební metodu Na účet zaplatit více, než je zbývající kreditní zůstatek objednávky. Pokud je například zbývající úvěrový zůstatek zákazníka 1000 $, ale objednávka má hodnotu 1 200 $, může zákazník zaplatit pomocí metody „na účet“ pouze 1 000 $. K zaplacení zůstatku musí zákazník použít jinou platební metodu. V budoucí verzi konfigurace Commerce umožní uživatelům při zadávání objednávek utrácet nad rámec jejich kreditního limitu.

Modul **Úvěry a inkasa** má nové možnosti správy úvěru. Chcete-li tyto funkce zapnout, povolte funkci **Správa úvěrů** v pracovním prostoru **Správa funkcí**. Jedna z nových funkcí umožňuje pozastavení prodejních objednávek na základě pravidel blokování. Osoba správce úvěru může poté po další analýze uvolnit nebo odmítnout objednávky. Možnost pozastavení prodejních objednávek se však nevztahuje na objednávky Commerce, protože prodejní objednávky mají často platbu předem a funkce **Správa úvěrů** zcela nepodporuje scénáře s předplacením. 

Bez ohledu na to, zda je funkce **Správa úvěrů** aktivována, prodejní objednávky nebudou pozastaveny, pokud zůstatek zákazníka během plnění objednávky překročí úvěrový limit. Místo toho Commerce vygeneruje buď varovnou nebo chybovou zprávu, v závislosti na hodnotě pole **Zpráva při překročení úvěrového limitu** na záložce **Úvěrové limity**.

Vlastnost **Vyloučit ze správy úvěrů**, která zabraňuje pozastavení prodejních objednávek Commerce, se nachází v záhlaví prodejní objednávky (**Maloobchod a obchod \> Zákazníci \> Všechny prodejní objednávky**). Pokud je tato vlastnost nastavena na **Ano** (výchozí hodnota) pro obchodní objednávky Commerce, budou objednávky vyloučeny z pracovního postupu pozastavení správy úvěru. Ačkoli je vlastnost pojmenována **Vyloučit ze správy úvěrů**, definovaný úvěrový limit bude při plnění objednávky stále využíván. Objednávky se prostě nepozastaví.

Schopnost pozastavit prodejní objednávky Commerce na základě pravidel blokování je plánována pro budoucí verze Commerce. Dokud to nebude podporováno, pokud musíte přinutit prodejní objednávky Commerce, aby prošly novými toky správy úvěru, upravte následující soubory XML ve svém řešení Visual Studio. V souborech upravte logiku tak, aby byl příznak **CredManExcludeSalesOrder** nastaven na **Ne**. Tímto způsobem nastavíte vlastnost **Vyloučit ze správy úvěrů** na **Ne** jako výchozí pro prodejní objednávky Commerce.

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

Pokud je příznak **CredManExcludeSalesOrder** nastaven na **Ne** a B2B zákazník může nakupovat v obchodech pomocí aplikace pokladního místa (POS), zaúčtování transakcí cash and carry může selhat. Například existuje pravidlo blokování typu platby v hotovosti a zákazník B2B nakoupil některé položky v obchodě pomocí hotovosti. V tomto případě nebude výsledná prodejní objednávka úspěšně fakturována, protože bude pozastavena. Proto se zaúčtování nezdaří. Z tohoto důvodu doporučujeme, abyste po implementaci tohoto přizpůsobení provedli komplexní testování.

## <a name="additional-resources"></a>Další prostředky

[Vytvoření webu elektronického obchodu B2B](set-up-b2b-site.md)

[Správa B2B obchodních partnerů pomocí zákaznických hierarchií](partners-customer-hierarchies.md)

[Správa uživatelů obchodních partnerů na webech elektronického obchodu B2B](manage-b2b-users.md)

[Nastavte limity množství produktů pro weby B2B elektronického obchodování](quantity-limits.md)

[SDK a aktualizace knihovny modulů](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
