---
title: Přehled správy zaměstnaneckých výhod
description: Tento článek obsahuje přehled funkce správy zaměstnaneckých výhod v modulu Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/06/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 261d71e955e4cb1a4a461d59725c631248e10b17
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227890"
---
# <a name="benefits-management-overview"></a>Přehled správy zaměstnaneckých výhod


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Chcete-li si zachovat konkurenceschopnost, musíte nabídnout bohatý soubor zaměstnaneckých výhod, abyste přilákali a udrželi své nejlepší zaměstnance. Kromě standardních výhod, jako je pojištění zdravotní a zubní péče, můžete také nabízet rozšířené služby, např. pomoc s adopcí, rekreační programy a příspěvky na ošacení. Funkce správy zaměstnaneckých výhod ve službě Microsoft Dynamics 365 Human Resources poskytuje flexibilní řešení, které podporuje širokou škálu možností zaměstnaneckých výhod. Aplikace Human Resources také zahrnuje snadno použitelné zaměstnanecké prostředí, které prezentuje vaše nabídky.

- Vylepšené plány zaměstnaneckých výhod vám umožňují vytvářet a spravovat jedinečné plány zaměstnaneckých výhod a podporovat složité tabulky sazeb zaměstnaneckých výhod a vnořené úrovně. Můžete snadno vytvářet programy, balíky a pravidla automatického zařazení pro zaměstnanecké výhody k usnadnění použití zaměstnancem.
- Programy flexibilních kreditů umožňují rozdělit podporu mezi důchod a další životní události.
- Rozsáhlá pravidla způsobilosti zajišťují poskytnutí správných zaměstnaneckých výhod odpovídajícím zaměstnancům.
- Online zařazení do zaměstnaneckých výhod poskytuje vašim zaměstnancům snadno použitelné prostředí.
- Kvalifikované zpracování životních událostí podporuje budoucí žívotní události.

Chcete-li získat přístup k ukázkovým datům, musíte znovu nasadit izolované testovací prostředí (sandbox).

> [!NOTE]
> Nyní můžete přizpůsobit stránky pro správu výhod. Vlastní pole související s mírou pokrytí lze přidat do stránky **Možnost pokrytí** pro plány výhod. Další informace o práci s vlastními poli naleznete v tématu [Vlastní pole](hr-developer-custom-fields.md).
>
> ![Vlastních pole správy výhod](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Povolení správy zaměstnaneckých výhod

Tento článek popisuje způsob, jakým lze zapnout funkce v aplikaci Human Resources. Také vysvětluje, které existující funkce v aplikaci Human Resources správa zaměstnaneckých výhod nahradí a které jsou zakázány po zapnutí správy zaměstnaneckých výhod.

> [!IMPORTANT]
> Po povolení Správy zaměstnaneckých výhod v **Produkčním** prostředí ji již nelze zakázat. Doporučujeme povolit a otestovat Správu zaměstnaneckých výhod v prostředí **Sandbox** před jejím povolením v **Produkčním** prostředí. Existují významné rozdíly mezi staršími funkcemi výhod a novými funkcemi pro správu výhod, které vyžadují další nastavení a měly by být testovány před uvedením do produkce.

Další informace naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

## <a name="process-overview"></a>Přehled procesu

Proces konfigurace výhod zahrnuje následující úkoly:

1.  Nastavte požadované informace o výhodách.
2.  Nastavte volitelné informace o výhodách.
3.  Nastavení plánů zaměstnaneckých výhod.
4.  Nastavení programů flexibilních kreditů (volitelné).
5.  Nakonfigurujte požadované informace o zaměstnancích.
6.  Nakonfigurujte volitelné informace o zaměstnancích.
7.  Zpracovat zaměstnance k určení způsobilosti.
8.  Zaměstnanci si vybírají plány prostřednictvím samoobsluhy zaměstnanců (volitelně).
9.  Potvrďte výběr plánu zaměstnanců.
10. Zpracování životní události (volitelné).
11. Aktualizace sazeb (volitelné).

## <a name="set-up-required-benefit-information"></a>Nastavte požadované informace o výhodách

Předtím, než mohou být zaměstnanci zapsáni do plánů, musí být nastaveno více komponent:

- **Parametry správy výhod** - Tato nastavení jsou sdílena mezi společnostmi. Můžete nastavit výchozí kódy důvodů, povolit možnost **Roční výplata zaměstnaneckých výhod**, nastavit výchozí frekvenci plateb pro nové zaměstnance a povolit životní události. Další informace naleznete v tématu [Nastavení parametrů správy zaměstnaneckých výhod](hr-benefits-setup-parameters.md).
- **Možnosti nároku na osobní kontakt** - Osobní kontakty jsou jednotlivci, kteří budou závislými osobami nebo příjemci plánů, které jsou zřízeny. Typicky jsou to děti, manželé nebo důvěryhodné organizace. Další informace viz [Konfigurace možností způsobilosti osobních kontaktů](hr-benefits-setup-contact-eligibility-options.md).
- **Možnosti pokrytí** - Nastavte typy pokrytí, které budou k dispozici pro plán. Konkrétně definujte, na koho by se mělo vztahovat pokrytí nebo kolik je k dispozici pokrytí. Další informace viz [Vytvoření možností pokrytí](hr-benefits-setup-coverage-options.md).
- **Typy plánů** - Nastavte typy plánů, které budou k dispozici při vytváření plánu výhod. Mezi příklady typů plánů patří **Zubní**, **Oční** a **Úspory**. Některá důležitá nastavení typu plánu určují nastavení, která jsou k dispozici v plánu výhod. Další informace viz [Vytvoření typů plánů](hr-benefits-setup-plan-types.md).
- **Pravidla způsobilosti** - Pravidla způsobilosti se používají k určení, zda má zaměstnanec nárok na plán. S každým plánem výhod musí být spojeno alespoň jedno pravidlo způsobilosti. Další informace viz [Konfigurace pravidel a možností způsobilosti](hr-benefits-setup-eligibility-rules.md).
- **Frekvence plateb** - Při konfiguraci sazeb výhod jsou vyžadovány frekvence plateb. Četnost plateb, která se používá na kurzu, pomáhá identifikovat částku, kterou zaměstnanec nebo zaměstnavatel dluží na týdenní, měsíční nebo roční bázi. Další informace naleznete v tématu [Nastavení frekvence plateb](hr-benefits-setup-payment-frequencies.md).
- **Sazby** - Sazby definují, kolik bude výhoda stát zaměstnance nebo zaměstnavatele. Pokud mají být peníze přiděleny zpět zaměstnanci (například kredit na členství v tělocvičně), je zadána záporná sazba. Další informace naleznete v tématu [Konfigurace sazeb](hr-benefits-setup-rates.md).
- **Úrovně sazeb** - Úrovně sazeb se používají, když se sazba musí změnit na základě některých kritérií. Nejběžnější úrovní sazeb je jednotlivá úroveň založená na věku. Lze však také nastavit dvojí úrovně sazeb, kde se sazba může změnit na základě pohlaví, věku nebo jiných kritérií.
- **Odpočty** - Odpočty jsou v zásadě informace / kódy záhlaví, které budou předány mzdovému systému za účelem identifikace odpočtu dávky. Tyto odpočty musíte nastavit, protože budou vyžadovány v plánu dávek. Další informace naleznete v tématu [Konfigurace odpočtů](hr-benefits-setup-deductions.md).
- **Období výhod** - Období výhod je období, kdy budou mít zaměstnanci krytí výhod. Je také známý jako plánovaný rok. Zde se také nastavují otevřené doby registrace.

## <a name="set-up-optional-benefit-information"></a>Nastavte volitelné informace o výhodách

K vytvoření plánu výhod není nutné nastavovat následující součásti:

- **Programy** - Program je soubor výhod, které se řídí stejnými pravidly způsobilosti. Například každý v obchodním oddělení může dostat mobilní telefon.
- **Sady** - Sada je skupina výhod, kde je nutné vybrat jeden plán, než bude k dispozici možnost výběru dalších plánů. Například vysoce odpočitatelný lékařský plán může být spojen s plánem účtu zdravotního spoření (HSA).
- **Typy životních událostí** - Životní události jsou události, které umožňují změnu v pokrytí zaměstnance. Typy životních událostí jsou propojeny s typem plánu. Například typ lékařského plánu může umožnit změny plánů z důvodu narození nebo adopce nebo z důvodu změny rodinného stavu. Typ pojistného plánu však nemusí umožňovat žádné změny z důvodu životních událostí. Další informace naleznete v tématu [Konfigurace typů životních událostí](hr-benefits-setup-life-event-types.md).
- **Čekací dny a čekací lhůty** - Čekací dobu pokrytí lze nastavit v plánu výhod. Například nově přijatý zaměstnanec může být schopen zapsat se k 401(k) až po třech měsících zaměstnání. V tomto případě je čekací doba tři měsíce. Čekací dny se používají v čekací době, pokud lze nové registrace zpracovat a odeslat poskytovateli pouze v konkrétní den v měsíci. Například pokud zápisy 401(k) lze zpracovat pouze patnáctého měsíce, po třech měsících zaměstnání je nastavená čekací doba tři měsíce a čekací den patnáctý. Další informace viz [Konfigurujte čekací dny](hr-benefits-setup-waiting-days.md) a [Konfigurujte čekací doby](hr-benefits-setup-waiting-periods.md).
- **Kódy důvodů** - Kódy důvodů se používají k vysvětlení, proč se pro zaměstnance může změnit výhoda. Další informace naleznete v tématu [Nastavení kódů důvodu](hr-benefits-setup-reason-codes.md).

## <a name="set-up-benefit-plans"></a>Nastavení plánů zaměstnaneckých výhod

Když nastavujete plán výhod, musíte před registrací zaměstnanců dokončit následující kroky:

- Přiřazení období zaměstnanecké výhody.
- Připojit možnosti pokrytí.
- Nastavte datum začátku platnosti a datum konce platnosti na kartě **Všeobecné**.
- Přiřaďte alespoň jedno pravidlo způsobilosti.
- Nastavte pole **Povolit/pokračovat v registraci** na kartě **Nastavení**.

Další informace o postupu při nastavení plánů zaměstnaneckých výhod získáte v tématu [Nastavení plánů zaměstnaneckých výhod](hr-benefits-plans-setup.md).

## <a name="set-up-flex-credit-programs-optional"></a>Nastavení programů flexibilních kreditů (volitelné)

Programy pružného kreditu umožňují registrovat zaměstnance k zaměstnaneckým výhodám podle předem stanoveného počtu pružných kreditů. Zaměstnanci si mohou vybrat způsob přidělení pružných kreditů. Například pokud jsou zaměstnanci již pojištěni v rámci plánu zdravotního pojištění svého manžela či manželky, nemusí používat své kredity pro zdravotní pojištění. Proto je možná budou chtít použít pro jiné výhody. Další informace o flexibilních kreditních programech viz [Nastavit flexibilní kreditní programy](hr-benefits-plans-flex-credit-programs.md).

## <a name="configure-required-employee-information"></a>Nakonfigurujte požadované informace o zaměstnancích

Před zapojením zaměstnanců do zaměstnaneckých výhod je nutné zadat požadované informace. 

Zaměstnanec musí mít přiřazenu **Pozici**. **Pozici** lze přiřadit zaměstnanci na stránce **Pracovník** nebo **Pozice** aktualizací hodnoty **Přiřazení pracovníka**. 

Dále musí být zaměstnanci registrování v plánu fixních odměn v den zahájení, nebo musí mít částku **Roční výše zaměstnaneckých výhod dle platu**. Před přidělením **Fixní kompenzace** k zaměstnanci musí být přiřazena **Pozice**. 

> [!NOTE] 
> **Počáteční datum fixní kompenzace** nesmí být před **Datem přiřazení pozice**.

Alternativně, pokud máte zaměstnance, který dostává dodatečné odměny, jako jsou provize, můžete přidat částku **Roční výplata zaměstnaneckých výhod** ze záznamu zaměstnance. Human Resources budou využívat částku **Roční výplata zaměstnaneckých výhod** při určování částek krytí, namísto částky **Fixní roční kompenzace**. **Roční výplata benefitů** musí platit od počátečního data zaměstnance nebo od začátku období zaměstnaneckých výhod, podle toho, co nastane dříve. K přiřazení **Roční výplaty zaměstnaneckých výhod** nicméně není vyžadována pozice. Chcete-li povolit funkci **Roční výplata zaměstnaneckých výhod**, přejděte na stránku **Sdílené parametry Human Resources** na kartě **Správa zaměstnaneckých výhod**. Tato funkce je ve výchozím nastavení vypnutá.

> [!IMPORTANT]
> Pokud jsou pro zaměstnance zadány obě částky **Fixní kompenzace** a **Roční výplata zaměstnaneckých výhod**, **Roční výplata zaměstnaneckých výhod** se použije při určování částky krytí. V sekci **Podrobnosti o zaměstnání** na stránce **Pracovník** musíte vybrat hodnotu v poli **Frekvence vyplácení zaměstnaneckých výhod**.

## <a name="configure-optional-employee-information"></a>Nakonfigurujte volitelné informace o zaměstnancích
Při vytvoření plánu zaměstnaneckých výhod, který používá sazby založené na pohlaví nebo věku, je nutné zadat datum narození a pohlaví zaměstnance pro výpočet nákladů na zaměstnanecké výhody.

## <a name="process-employees-to-determine-eligibility"></a>Zpracovat zaměstnance k určení způsobilosti
Předtím, než se zaměstnanci mohou zaregistrovat do plánů, je spuštěno zpracování způsobilosti, aby se zjistilo, pro které plány mají nárok. Výsledky procesu způsobilosti si můžete prohlédnout v **Prohlížeči výsledků procesu**. Další informace naleznete v tématu [Zpracování způsobilosti k registraci](hr-benefits-process-enrollment-eligibility.md).

## <a name="employees-select-plans-using-employee-self-service-optional"></a>Zaměstnanci si vybírají plány prostřednictvím **samoobsluhy pro zaměstnance** (volitelně)

Když dojde k otevřené registraci, zaměstnanci jsou nově najati nebo dojde k životní události, zaměstnanci si mohou vybrat nebo aktualizovat své zaměstnanecké výhody prostřednictvím **samoobsluhy pro zaměstnance**. Další informace viz [Konfigurace samoobsluhy pro zaměstnance](hr-benefits-setup-employee-self-service.md).

## <a name="confirm-employee-plan-selections"></a>Potvrďte výběr plánu zaměstnanců

Výhody, které si zaměstnanci vyberou, musí být potvrzeny, než budou zaměstnanci považováni za zapsané v nich. Výhody lze vybrat také jménem zaměstnance. Chcete-li vybrat nebo potvrdit výhody, na stránce **Zaměstnanec** na kartě **Zamšstnanecké výhody** vyberte **Plány zaměstnaneckých výhod**. Chcete-li vybrat nebo potvrdit výhody pro více zaměstnanců, použijte stránku **Hromadná aktualizace plánů zaměstnaneckých výhod**.

## <a name="life-event-processing-optional"></a>Zpracování životní události (volitelné)

Během životního cyklu zaměstnance se každý zaměstnanec může setkat s různými životními událostmi, jako je manželství, změny v zaměstnání nebo změny závislých osob nebo příjemců. Chcete-li používat životní události, musíte je povolit na stránce **Sdílené parametry lidských zdrojů**. Nastavte typy životních událostí a možnosti životních událostí pro typy plánů.

Než bude možné zpracovat životní události, musí být v průběhu doby náboru alespoň jednou spuštěna možnost otevřít registraci. V USA je otevření registrace obvykle jednou za rok. Mimo USA může být otevření registrace spuštěno v době nástupu do zaměstnání. Zpracování životních událostí nevyžaduje, aby pracovníci vybrali plán výhod. Pracovníci však musí být zahrnuti do zpracování otevřené registrace. Další informace naleznete v následujících tématech:

- [Zpracování životních událostí](hr-benefits-process-life-events.md)
- [Zpracování změn životních událostí](hr-benefits-process-life-event-changes.md)
- [Zpracování způsobilosti k životním událostem](hr-benefits-process-life-event-eligibility.md)

Po dokončení zpracování životní události a po dobu, kdy je otevřeno období registrace životní události, mohou zaměstnanci provádět změny možností plánu, které jsou ovlivněny životní událostí. Správci mohou provádět změny jménem zaměstnanců. Poté, co skončí období registrace a s transakcí životní události nesouvisí žádné nepotvrzené typy plánu, je transakce uzavřena.

Všechny plány, které jsou ovlivněny životní událostí, musí být buď vybrány, nebo vzdány a následně potvrzeny. Pokud plán není vybrán, není vzdán, a proto není potvrzen, transakce životní události se neuzavře.

Správci mohou transakci životní události podle potřeby ručně uzavřít tak, že ji vyberou a poté vyberou **Zavřít**. Pokud transakce obsahuje nepotvrzené plány a správce ji chce uzavřít, uzavření životní události může omezit úpravy těchto plánů.

Uzavřené životní události nelze smazat.

Správci mohou transakci životní události podle potřeby znovu otevřít tak, že ji vyberou a poté vyberou **Znovu otevřít**.

## <a name="rate-updates-optional"></a>Aktualizace sazeb (volitelné)

Někdy se sazba výhod během období plánu mění. Chcete-li aktualizovat sazby pro zaměstnance, kteří jsou již zapsáni v plánu, musíte zpracovat změny sazby. Další informace naleznete v tématu [Zpracování změn sazeb](hr-benefits-process-rate-changes.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
