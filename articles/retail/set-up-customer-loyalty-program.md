---
title: Přehled věrnostního programu
description: Toto téma popisuje funkce věrnostního programu v aplikaci Microsoft Dynamics 365 for Retail odpovídající kroky nastavení, které pomáhají maloobchodníkům začít se svými věrnostními programy.
author: scott-tucker
manager: AnnBe
ms.date: 01/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16201
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: bb1a1ff28c846a35858df971e29bb7a551c8012a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "320114"
---
# <a name="loyalty-overview"></a>Přehled věrnostního programu

[!include [banner](includes/banner.md)]

Věrnostní programy mohou posílit věrnost odběratele pomocí odměn odběratelům za jejich interakce se značkou maloobchodníka. V aplikaci Microsoft Dynamics 365 for Retail můžete nastavit jednoduché nebo komplexní věrnostní programy, které platí pro různé právnické osoby v libovolné maloobchodní síti. Toto téma popisuje funkce věrnostního programu v aplikaci Microsoft Dynamics 365 for Retail odpovídající kroky nastavení, které pomáhají maloobchodníkům začít se svými věrnostními programy.

Věrnostní program lze nastavit tak, aby zahrnoval následující možnosti.

- Nastavte více typů odměn, které ve věrnostních programech nabízíte, a sledujte účast ve věrnostních programech.
- Nastavte věrnostní programy, které reprezentují různé motivační odměny, které nabízíte. Je možné zahrnout vrstvy věrnostního programu, aby nabízely větší pobídky a odměny zákazníkům, kteří ve vaši obchodech nakupují častěji nebo utrácejí více peněz.
- Definujte pravidla získávání pro identifikaci aktivit, které zákazník musí provést, pokud chce získat odměny. Můžete také definovat pravidla využití a určit, kdy a jak může zákazník odměny uplatnit.
- Vydávejte věrnostní karty z maloobchodní sítě, která se účastní vašich věrnostních programů, a propojte jeden nebo více věrnostních programů, kterých se mohou odběratelé zúčastnit. Můžete také propojit záznam zákazníka na věrnostní kartu tak, aby zákazník mohl sbírat dohromady věrnostní body z více karet a uplatňovat je.
- Ručně upravte věrnostní karty nebo převeďte zůstatek věrnostních odměn z jedné karty na druhou za účelem uložení bodů nebo odměnění zákazníka.

## <a name="setting-up-loyalty-programs"></a>Nastavení věrnostních programů

Je nutné nastavit několik součástí, aby bylo možné funkci věrnostního programu v aplikaci Dynamics 365 for Retail zapnout. Následující diagram znázorňuje věrnostní součásti a jejich vzájemný vztah.

![Tok procesu nastavení věrnostního programu](./media/loyaltyprocess.gif "Komponenty věrnostního programu a jak spolu souvisí mezi sebou")

## <a name="loyalty-components"></a>Věrnostní komponenty

V následující tabulce jsou popsány jednotlivé komponenty a jejich použití v rámci nastavení věrnostního programu.

| Komponenta                                        | popis | Kde se používá |
|--------------------------------------------------|-------------|-----------------|
| Nastavení slev (předpoklad)                  | Nastavte slevy, které nabízíte věrným zákazníkům. Například můžete nabídnout 5 % z ceny všech oděvů. | Slevy musí být přidány do cenových skupin, aby je bylo možné zahrnout do věrnostního programu. Cenové skupiny jsou jsou přiřazeny věrnostním programům a úrovním věrnostních programů. |
| Nastavit cenové skupiny (předpoklady)               | Cenové skupiny se používají k vytváření a správě cen a slev maloobchodních produktů. Nastavte cenové skupiny, které zahrnují slevy pro vaše věrnostní programy. | Cenové skupiny jsou přiřazeny k věrnostním programům a úrovním věrnostních programů. |
| Nastavení kanálů (předpoklad)                   | Maloobchodní kanály jsou obchody, které jsou zapojeny do věrnostních programů, například kamenné obchody, online obchody nebo kontaktní střediska. Maloobchodní kanály je třeba nastavit, než je bude možné přiřadit věrnostním programům. | Maloobchodní sítě přiřaďte věrnostnímu programu, pokud je maloobchodní síť zapojen do věrnostního programu. |
| Nastavení platební metody věrnostního programu (předpoklad) | Předtím, než je možné věrnostní kartu použít u pokladny a věrnostní body uplatnit jako součást věrnostního schématu, musíte nastavit způsob platby. Platební metodu věrnostního programu je třeba přidat také do maloobchodní, aby mohli odběratelé uplatnit své věrnostní body jako platbu za produkty. | Nastavte způsob platby věrnostního programu a poté přiřaďte způsob platby věrnostního programu maloobchodním kanálům, které jsou do věrnostního programu zapojeny. |
| Nastavit časové intervaly                            | Časové intervaly umožňují pružné nastavení časového intervalu, který se vztahuje na úrovně věrnostního programu. Použijte časové intervaly k určení, jak dlouho odběratel může zůstat na úrovni nebo za jakou dobu musí odběratel dokončit aktivitu pro získání nároku na určitou úroveň. | Časové intervaly platí, pouze pokud ve věrnostních programech používáte úrovně. Vyberte časový interval vztahující se k úrovni programu a časové intervaly, které se týkají pravidel úrovně programu. |
| Nastavení bodů odměn                             | Body odměn jsou typy odměn, které odběratelům nabízíte. Body odměny lze uplatnit nebo neuplatnit. Uplatnitelné body odměny lze vyměnit za výrobky. Neuplatnitelné body odměny se používají pro účely sledování a k tomu, aby odběratel mohl přejít na další úroveň ve věrnostním programu. | Na body odměn odkazují pravidla úrovně a slouží ke kvalifikaci zákazníka pro určitou úroveň. Body odměn jsou odkazovány také ve schématech věrnostních programů v pravidech získávání a využití. V pravidlech získávání určete odměny, které může odběratel za určité aktivity získat. V pravidlech využití určete odměny, které může odběratel uplatnit. |
| Nastavení věrnostních programů                          | Věrnostní programy jsou základní věrnostní entitou, kterou nabízíte. Každý věrnostní program může mít také přiřazené úrovně věrnostního programu. Slevy a cenové skupiny jsou přiřazeny k věrnostním programům na úrovni programu nebo na úrovni vrstvy (úrovně). | Věrnostní schémata vytvořte pro věrnostní programy. Přiřaďte věrnostní karty pro věrnostní programy. Věrnostní karty lze přiřadit odběrateli. Maloobchodní kanály se mohou zapojit do věrnostních programů přiřazených věrnostním schématům. Zákazník, který je držitelem věrnostní karty, se může zapojit do věrnostních programů, které jsou k dané kartě přiřazeny. |
| Nastavení věrnostních úrovní a pravidel úrovní              | Věrnostní úrovně jsou volitelné úrovní, které můžete definovat pro věrnostní programy. Můžete nastavit základní slevy a odměny pro všechny zákazníky, kteří se věrnostního programu účastní, a můžete nastavit další slevy a odměny pro zákazníky, kteří dosáhnou různé úrovně v programu. Pro každou úroveň věrnostního programu, kterou definujete, můžete nastavit pravidla, která zákazníka kvalifikují pro danou úroveň. Můžete také definovat, jak dlouho zákazník může zůstat na této úrovni, až jí dosáhne. | Věrnostní úrovně a pravidla věrnostní úrovně jsou definovány ve věrnostních programech. Pokud nedefinujete žádné věrnostní úrovně, všichni odběratelé, kteří se účastní věrnostního programu, se kvalifikují pro slevy, které přiřadíte v cenové skupině věrnostního programu. Pokud definujete věrnostní vrstvy, můžete nastavit pravidla získávání a využití pro věrnostní úrovně ve věrnostním schématu. |
| Nastavení věrnostních schémat                           | Věrnostní schémata určují pravidla získávání a využití, která se týkají vybraného věrnostního programu. Přiřaďte maloobchodní kanály věrnostnímu schématu a určete, který věrnostní program, pravidla získávání a využití pro maloobchod platí. | Věrnostní schéma je přiřazeno k věrnostnímu programu a maloobchodní síti. Stejnému věrnostnímu programu můžete přiřadit více věrnostních schémat a mnoho věrnostních schémat můžete přiřadit několika maloobchodním sítím. |
| Nastavení věrnostních karet                             | Věrnostní karta opravňuje držitele karty zapojit se do věrnostních programů, které jsou k dané kartě přiřazeny. Věrnostní karty lze vydat anonymně nebo mohou být přiřazeny určitému odběrateli. Můžete zobrazit transakce věrnostní karty pro konkrétní kartu a zobrazit souhrn věrnostních bodů, které byly na kartě nasbírány. Lze vydávat věrnostní karty ze všech maloobchodních sítí. Můžete také ručně upravit věrnostní kartu, aby odběratel mohl přejít na jinou úroveň, přidat věrnostní body nebo převést zůstatek věrnostních bodů z jedné karty na druhou. | Věrnostní programy můžete přiřadit věrnostní kartě. |

## <a name="loyalty-processes"></a>Věrnostní procesy

Následující tabulka popisuje procesy, které je nutné provést k odeslání konfigurací a dat věrnostních programů do obchodů a k načtení transakcí věrnostních programu z obchodů.

| Název procesu                         | Popis | Název webové stránky |
|--------------------------------------|-------------|-----------|
| 1050 (informace o věrnostním programu)           | Spuštěním tohoto procesu odešlete data konfigurace věrnostního programu z aplikace Dynamics 365 for Retail do maloobchodů. Je vhodné naplánovat časté spouštění tohoto procesu, aby data věrnostních programů byla odesílána do všech obchodů. | Plán distribuce |
| Zpracovat věrnostní schémata              | Spuštěním tohoto procesu lze přidružit věrnostní schémata maloobchodním sítím, ke kterým je přiřazeno věrnostní schéma. Tento proces může být naplánován jako dávkový proces. Tento proces musíte spustit při změně dat konfigurace věrnostních programů, například věrnostních schémat, věrnostních programů nebo bodů věrnostních odměn. | Zpracovat věrnostní schémata |
| Zpracovat věrnostní transakce offline | Spusťte tento proces, chcete-li aktualizovat věrnostní karty, aby zahrnovaly transakce, které byly zpracovány offline. Tento postup se použije pouze v případě, že zaškrtnete políčko **Získat offline** na stránce **Sdílené parametry maloobchodu**, aby bylo možné odměny získat offline. | Zpracovat věrnostní transakce offline |
| Aktualizovat úrovně věrnostních karet            | Spusťte tento proces, chcete-li vyhodnotit aktivitu získávání odběratele ve srovnání s pravidly úrovně pro věrnostní program a aktualizovat stav úrovně odběratele. Tento proces je nutný pouze v případě, že změníte pravidla úrovně ve věrnostních programech a chcete aktualizovaná pravidla zpětně použít na věrnostní karty, které již byly vystaveny. Tento proces může být naplánován jako dávkový proces nebo pro jednotlivé karty. | Aktualizovat úrovně věrnostních karet |

## <a name="loyalty-enhancements"></a>Vylepšení věrnostního programu

Retail obsahuje novou funkci věrnostního programu jako součást verze z října 2018. Každé z nových vylepšení je popsáno níže.

- V rámci věrnostního schématu v předchozích verzích mohli maloobchodníci vytvářet různá pravidla získávání a uplatnění podle úrovní, aby odlišili odměny pro zákazníky v různých úrovních. Maloobchodníci mohou nyní zahrnovat „přidělení“ jako součást pravidel získávání a uplatnění tak, aby určitá skupina zákazníků mohla být součástí stávajících úrovní, ale přesto odměňována jiným způsobem. Díky tomu není třeba vytvářet další úrovně.
    
    > [!NOTE]
    > Pravidla příjmu v rámci věrnostního schématu jsou dodatečná. Například pokud vytvoříte pravidlo pro odměnu člena zlaté úrovně 10 bodů za každý americký dolar a také vytvoříte pravidlo pro zákazníka s přidělením veterána na odměnu za 5 bodů za každý dolar, pak veterán, který je také členem zlaté úrovně získá 15 bodů za 1 americký dolar, jelikož se zákazník kvalifikuje pro obě podmínky. Nicméně pokud by veteránský zákazník nebyl členem zlaté úrovně, pak by získal 5 bodů za každý dolar. Aby se projevily změny v kanálu, spusťte úlohy **Zpracovat věrnostní schémata** a **1050** (informace o věrnostním programu).
    
    ![Příjmy podle přidělení](./media/Affiliation%20based%20earning.png "Příjmy podle přidělení")

- Maloobchodníci mají často speciální ceny pro určitou skupinu zákazníků, na kterou nechtějí používat věrnostní programy. Například velkoobchodníci nebo zaměstnanci, kteří dostávají zvláštní ceny a žádné věrnostní body. Běžně se „přidělení“ používají pro poskytnutí zvláštních cen takovým skupinám zákazníků. Pro omezení určité skupiny odběratelů při získávání věrnostních bodů může prodejce určit jedno nebo více přidělení v části věrnostního schématu **Vyloučená přidělení**. Tímto způsobem, když jsou zákazníci patřící do vyloučených přidělení stávajícími věrnostními členy, nebudou moci získat za své nákupy věrnostní body. Aby se projevily změny v kanálu, spusťte úlohy **Zpracovat věrnostní schémata** a **1050** (informace o věrnostním programu).

    ![Vyloučená přidělení](./media/Excluded%20affiliations.png "Vyloučit přidělení ze získávání věrnostních bodů")
    
- Maloobchodní prodejci mohou generovat čísla věrnostních karet v kanálech. Před aktualizací v říjnu roku 2018 mohli maloobchodníci použít fyzické věrnostní karty nebo vygenerovat věrnostní kartu pomocí některých jedinečných informací o zákaznících, jako je například telefonní číslo. Chcete-li povolit automatické generování věrnostních karet v maloobchodních prodejnách, zapněte **Generovat číslo věrnostní karty** ve funkčním profilu, který je přidružen k obchodu. Pro online kanály mohou maloobchodní prodejci použít API rozhraní IssueLoyaltyCard pro vystavení věrnostních karet zákazníkům. Maloobchodní prodejci mohou buď zadat číslo věrnostní karty do tohoto rozhraní API, které se použije ke generování věrnostní kartu, nebo systém použije posloupnost čísel věrnostních karet v aplikaci Dynamics 365 for Retail. Pokud však není číselná řada k dispozici a prodejce neposkytne číslo věrnostní karty při volání rozhraní API, zobrazí se chyba.

    ![Generování věrnostní karty](./media/Generate%20loyalty%20card.png "Automatické vygenerování čísla věrnostní karty")

- Získané a uplatněné věrnostní body jsou nyní ukládány pro každou transakci a prodejní objednávky proti řádku prodeje, takže je možné refundovat nebo vzít zpět stejnou částku v případě úplného nebo částečného vrácení. Navíc viditelnost bodů na úrovni řádku prodej poskytuje uživatelům kontaktního střediska možnost odpovědět na otázky zákazníků o tom, kolik bodů bylo získáno nebo uplatněno za každý řádek. Před touto změnou byly body odměn vždy přepočítány během vrácení, což vedlo k odlišné částce než původní, pokud se změnila pravidla získávání nebo uplatnění, a také uživatelé kontaktního střediska neměli viditelnost v rozdělení bodů. Body lze zobrazit ve formuláři **Transakce karty** pro každou věrnostní kartu.    
- Maloobchodní prodejci nyní mohou určit období připsání pro každý bod odměny. Konfigurace období připsání určí trvání od data získání, po kterém budou k dispozici body odměny pro zákazníky. Neudělené body lze zobrazit ve sloupci **Neudělené body** na stránce **Věrnostní karty**. Maloobchodní prodejci kromě toho mohou definovat maximální limit bodů věrnostní odměny na věrnostní kartu. Toto pole lze použít ke snížení dopadu podvodu s věrnostními body. Po dosažení maximálního počtu bodů odměn nemůže uživatel získat další body. Prodejce se může rozhodnout takovou kartu blokovat, dokud neprošetří možný podvod. Pokud prodejce zjistí podvod, nemůže pouze zablokovat věrnostní kartu zákazníka, ale musí také označit zákazníka jako blokovaného. To se provede nastavením vlastnosti **Blokovat zákazníka pro registraci k věrnostnímu programu** na **Ano** v rámci možnosti **Všichni odběratelé** na pevné záložce **Maloobchod**. Blokovaným zákazníkům nebude možné vystavit věrnostní kartu v žádném z kanálů.

    ![Připsání bodů a jejich maximální počet](./media/Vesting%20and%20maximum%20reward%20points.png "Definování připsání bodů a jejich maximálního počtu")

- Přidělení se používají k poskytnutí speciálních cen a slev, ale existují některá přidělení, u kterých maloobchodní prodejci nechtějí, aby je viděli zákazníci. Například přidělení s názvem Zákazník s vysokou útratou nemusí být některými zákazníky dobře vnímáno. Kromě toho existují určitá přidělení, která by neměla být spravována v obchodě, například zaměstnanci, protože nechcete, aby pokladníci rozhodovali o tom, kdo je zaměstnancem a tudíž poskytovali slevy na základě zaměstnání. Maloobchodní prodejci nyní mohou vybrat přidělení, která mají být skryta ve maloobchodní síti. Umístění označen jako **Skrýt v kanálech** nelze zobrazit, přidat nebo odebrat v POS. Ceník a slevy přidružené k přidělení se však na produkty budou i nadále vztahovat.

    ![Skrýt přidělení](./media/Hide%20affiliations.png "Skrýt přidělení v kanálech")
    
- Uživatelé kontaktního střediska mohou nyní snadněji vyhledat zákazníka pomocí informací o jeho věrnostní kartě a přejít na stránky věrnostní karty zákazníka a stránky transakcí věrnostních karet ze stránky **Odběratelský servis**.

    ![Odběratelský servis](./media/Customer%20service.png "Vyhledat informace o věrnostním programu pro zákazníka")
    
- Pokud je věrnostní karty porušena, je třeba vygenerovat náhradní kartu a převést existující body na novou kartu. V této verzi byl tok náhrady karty zjednodušen. Navíc zákazníci mohou věnovat některé nebo všechny své věrnostní body přátelům nebo rodině. Když jsou body převedeny, položky úprav bodů jsou vytvořeny pro jednotlivé věrnostní karty. K funkcím náhradní karty a převodu zůstatku lze přistoupit ze stránky **Věrnostní karty**.

    ![Náhrada a převod bodů](./media/Replace%20and%20transfer%20points.png "Náhrada věrnostní karty nebo převod zůstatku")
    
- Maloobchodní prodejci mohou chtít zaznamenat účinnost určitého kanálu pro registraci zákazníků do věrnostního programu. Zdroj registrace pro věrnostní karty je nyní uložen, aby maloobchodní prodejci mohli na těchto datech spouštět sestavy. Zdroj registrací je automaticky zaznamenán pro všechny vydané věrnostní karty z kanálů MPOS/CPOS nebo e-Commerce. Pro věrnostní karty vydané z aplikace účetního systému může uživatel kontaktního střediska vybrat příslušný kanál.
- V předchozích verzích maloobchodní prodejci mohli použít MPOS/CPOS pro uplatnění věrnostních bodů pro zákazníky v obchodě. Nicméně v těchto verzích, protože věrnostní zůstatek je zobrazen ve věrnostních bodech, pokladník nemohl zobrazit částku hodnoty měny, která by mohla být použita na aktuální transakci. Pokladník musel před vyplacením podle věrnostních bodů provést měnový převod bodů. V aktuálním vydání, po přidání řádků do transakce, může pokladník zobrazit částku, kterou věrnostní body mohou pokrýt pro aktuální transakci, což usnadňuje použití některých nebo všech věrnostních bodů na transakci. Navíc může pokladník zobrazit body, které vyprší v příštích 30 dnech, takže mohou provést následný a křížový prodej pro motivaci zákazníka, aby utratil body, jejichž platnost vyprší, při této transakci.

    ![Body pokryté věrnostním zůstatkem](./media/Points%20covered%20by%20loyalty%20balance.png "Zobrazit zůstatek pokrytý věrnostními body")

    ![Body s končící platností](./media/Expiring%20points.png "Zobrazení bodů s končící platností")
    

- Ve verzi 8.1.3 jsme povolili možnost platby podle věrnosti v kanálu telefonického centra. Chcete-li tuto možnost povolit, vytvořte typ věrnostní úhrady a spojte ho s kontaktním střediskem. 

>[!NOTE]
> Vzhledem k tomu, že věrnostní platby jsou nastaveny jako platby kartou, je nutné vybrat kartu ze stránky **nastavení karty**. 

![Nastavení věrnostní karty](./media/LoyaltyCardSetup.png "Nastavení věrnostní karty")

Po tomto nastavení mohou zákazníci znovu uplatnit své věrnostní body v kontaktním středisku. Dále vylepšujeme možnosti uživatelů na zobrazení částky pokryté věrnostními body, aby nemuseli uživatelé kontaktních středisek přecházet na jinou obrazovku, aby mohli zobrazit zůstatek věrnostních bodů.

- Mnoho maloobchodníků přiděluje věrnostní body pouze na základě prodejních transakcí, ale maloobchodníci více zaměření na zákazníka chtějí odměnit své zákazníky za jakoukoli aktivitu s jejich značkou. Například chtějí poskytnout odměny za vyplnění online průzkumu, návštěvu obchodu, přidělení značky Líbí se mi pro prodejce ve službě Facebook nebo tweetování o prodejci. Maloobchodní prodejce proto může definovat libovolný počet v okně Jiný typ aktivity a definovat odpovídající pravidla získávání bodů za tyto aktivity. Existuje také rozhraní API maloobchodního serveru "PostNonTransactionalActivityLoyaltyPoints", které lze volat, když je identifikovaná aktivita, která by měla odměnit zákazníka věrnostními body. Toto rozhraní API předpokládá ID věrnostní karty, ID kanálu a ID jiného typu aktivity, aby bylo možné vyhledat zákazníka, který by měl být odměněn, a aby bylo možné identifikovat pravidlo pro ocenění za aktivitu. 

    Obecně mají body za odměnu u aktivit mimo transakce dva hlavní kroky:
    - Realizace aktivity, která by měla být oceněna.
    - Udělení příslušných bodů.

    První krok je externí k aplikaci Microsoft Dynamics 365 for Retail, například tweet o značce nebo označení značky To se mi líbí ve službě Facebook. Po rozpoznání této aktivity mohou prodejci volat výše uvedené rozhraní API maloobchodnío serveru a udělit věrnostní body v reálném čase. V takovém případě není nutné provést krok kontroly vzhledem k tomu, že se aktivita uskutečnila a měly by být uděleny příslušné body. Existují však situace, kdy by chtěl prodejce zkontrolovat záznamy předtím, než body udělí. Prodejce například zavedl dílnu v prodejně, pro kterou se zákazníci přihlašují na webu elektronického obchodování nebo v jiné aplikaci pro registraci akcí. Věrnostní body však mohou získávat pouze zákazníci, kteří se dostaví. U takových scénářů jsme ve verzi 10.0 zavedli datovou entitu nazvanou **Ostatní řádky typu maloobchodní aktivity**. Tato entita data umožňuje maloobchodním prodejcům použít rámec importu/exportu dat (DIXF) nebo rozhraní API OData k záznamu aktivit, které mají odměnit odběratele věrnostními body. Entita dat obsahuje aktivity v deníku s názvem **věrnostní řádky pro ostatní aktivity**, které lze použít pro účely přezkoumání a úpravy. Poté, co bylo zkontrolováno data IT uživatele, lze ručně zaúčtovat řádky aktivity nebo spustit úlohu s názvem **zpracovat jiný typ aktivity pro věrnostní řádky**, které zaúčtují všechny řádky nezaúčtované aktivity a body odměny pro odběratele na základě pravidla příjmů. Ve výše uvedeném scénáři bude aplikace registrace události volat rozhraní OD API k odeslání informací o zákazníkovi do aplikace Dynamics 365 for Retail. Uživatel IT však může zaúčtovat řádky aktivity pro zákazníky, kteří navštívili seminář a odstranit řádky aktivity pro ostatní zákazníky. 

> [!NOTE]
> V současné době vynutí systém po uživateli, aby nastavil číselnou řadu pro "ostatní typy aktivit", ale nebude se jednat o povinný krok v příštích verzích. Chcete-li nastavit číselnou řadu, přejděte na **Sdílené maloobchodní parametry > číselné řady** a vyberte číselnou řadu pro **ID typu ostatních věrnostních aktivit**.

- Pokud chcete poskytovat zákaznické služby a efektivně řešit dotazy zákazníků, je důležité, aby měli podkladní přístup k úplnému profilu zákazníka. Ve verzi 10.0 budou pokladní moci zobrazit detaily věrnostní historie spolu s přidruženým věrnostním programem a informacemi o vrstvě v POS.
- Dodání zdarma nebo se slevou je jedním z vysoce motivačních faktorů pro zákazníky při nákupu online. Abychom umožnili maloobchodním prodejcům nastavení propagačních dodávek ve verzi 10.0, zavádíme nový typ promoakce nazvaný Sleva prahové hodnoty expedice, v němž může prodejce definovat prahové hodnoty, které při splnění kvalifikují zákazníka na bezplatné nebo zlevněné dodání. Například při útratě 35 USD získáte dopravu do dvou dnů zdarma nebo Bezplatná expedice do dvou dnů pro všechny věrné zákazníky Tyto slevy se vztahují pouze k poplatkům za expedici objednávek. Vzhledem k tomu, že maloobchodní prodejce může nastavit více typů poplatků, jako je manipulační nebo instalační poplatek, musí určit, který poplatek je považován za poplatek za expedici. Tato konfigurace je nazvána "Kód dopravného" a je k dispozici na kartě **Zakázky odběratele** na stránce **parametry maloobchodu**. Tato sleva uznává všechny existující standardní možnosti slevy, jako je například umožnění prodejci omezit tyto slevy na poukazy, aby je získal pouze zákazník s poukazy. Tyto slevy také využívají schopnost cenové skupiny ceny k určení nároku na tyto slevy. Například prodejce může spustit tyto promoakce, pouze v online kanálech nebo napříč kanály pro určité skupiny zákazníků, jako jsou věrní zákazníci. Jakmile řádky objednávky s určeným režimem dodání splní definovanou prahovou hodnotu, použije se sleva za doručení a sníží se poplatek za doručení na základě nastavené slevy. 

> [!NOTE]
> Na rozdíl od jiných časových slev, jako je například množství, jednotlivý produkt, shoda a porovnání a slevy prahové hodnoty, nevytvoří sleva za doručení řádky slevy a úpravy poplatku za dopravu je nutné provést přímo.
