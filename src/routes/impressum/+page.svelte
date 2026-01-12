<script>
  import {onMount} from "svelte";

  let backgroundImage;
  let heroSection;
  let logo;
  let logoPosition;

  onMount(() => {
    logoPosition = heroSection.clientHeight - backgroundImage.clientHeight - (logo.clientHeight / 4.25);
    backgroundImage.play();
  });

</script>

<section id="hero" bind:this={heroSection}>
    <video class="section--background" autoplay muted playsinline loop bind:this={backgroundImage}>
        <source src="videos/header.webm" type="video/webm">
        <source src="videos/header.mp4" type="video/mp4">
    </video>
    <img class="logo" src="logo_claim.svg">
    <svg id="logo-large" xmlns="http://www.w3.org/2000/svg" version="1.1" viewBox="0 0 921.8 520" width="921.8" height="520" style="--logo-bottom: {logoPosition}px" bind:this={logo}>
        <defs>
            <pattern id='image' width="1" height="1" viewBox="0 0 100 100" preserveAspectRatio="none">
                <image xlink:href='/images/logo_background.jpg' width="100" height="100" preserveAspectRatio="none"></image>
            </pattern>
        </defs>
        <path class="st0" d="M155,57.2c-14.8-5.2-31.2,2.1-36.6,16.4L0,394.9h60.5L172.1,92.3c5.4-14.2-2.2-29.9-17.1-35.1Z"/>
        <path class="st0" d="M453.1,483.3L265,18c-5.4-14.2-21.8-21.5-36.6-16.3-14.8,5.2-22.4,20.9-17.1,35.1l105.8,261.5h-120.5c-15.8,0-28.6,12.3-28.6,27.4s12.8,27.4,28.6,27.4h142.6l60.3,149c5.4,14.2,21.8,21.5,36.6,16.3,14.8-5.2,22.4-20.9,17.1-35.1Z"/>
        <path class="st0" d="M893.3,54.8c-15.8,0-28.5,12.2-28.5,27.4v187.7h-274.5V27.5c0-15.1-12.8-27.4-28.5-27.4s-28.6,12.3-28.6,27.4v367.4h57.1v-70.3h274.5v125.5c0,15.1,12.8,27.4,28.5,27.4s28.5-12.2,28.5-27.4V82.2c0-15.1-12.8-27.4-28.5-27.4Z"/>
    </svg>
</section>
<main>
    <section id="imprint">
        <div class="text-section">
            <h1>Impressum</h1>
            <h2>Diensteanbieter</h2>
            <p>Andreas Ha&szlig;ler, Ha&szlig;ler-Schwenk-Weiss GbR</p>
            <p>Gottlieb-Daimler Stra&szlig;e 11</p>
            <p>89150 Laichingen</p>

            <h2>Kontaktm&ouml;glichkeiten</h2>
            <p>E-Mail-Adresse: <a href="mailto:info@ahstuckdesign.de">info@ahstuckdesign.de</a></p>
            <p>Telefon: +49 7333 8053144</p>

            <h2>Angaben zum Unternehmen</h2>
            <p>Umsatzsteuer Identifikationsnummer (USt-ID): DE452011847</p>

            <h2>Berufshaftpflicht&shy;versicherung</h2>
            <p>SV Sparkassenversicherung,<br>
                Sitz Stuttgart, Deutschland<br>
                Registergericht Stuttgart<br>
                HRB 16264</p>
            <p>R&auml;umliche Geltung: EU</p>

            <h2>Kammer</h2>
            <p>Kammer (oder vergleichbare berufsrechtlicher Organisation): </p>
            <p>Handwerkskammer Ulm<br>Olgastra&szlig;e 72<br>89073 Ulm<br>Deutschland</p>
            <p>Website und Kontakt der Kammer: <a href="https://www.hwk-ulm.de/" target="_blank">https://www.hwk-ulm.de/</a></p>

            <h2>Vorbehalt der Nutzung f&uuml;r Text und Data Mining</h2>
            <p>Vorbehalt der Nutzung f&uuml;r Text und Data Mining: Der Inhaber dieser Website gestattet die Nutzung oder das Herunterladen von Inhalten dieser Website durch Dritte f&uuml;r die Entwicklung, das Training oder den Betrieb von k&uuml;nstlicher Intelligenz oder anderen maschinellen Lernsystemen ("Text und Data Mining") ausschlie&szlig;lich mit ausdr&uuml;cklicher schriftlicher Zustimmung des Inhabers. Ohne eine solche Zustimmung ist es untersagt, die Inhalte f&uuml;r Text und Data Mining zu verwenden. Dies gilt auch, wenn auf der Website keine Meta-Angaben vorhanden sind, die entsprechende Verfahren aussperren, und selbst dann, wenn Bots, die den Zweck haben, die Website zu Zwecken des Text und Data Mining auszulesen, nicht ausgesperrt werden.</p>

            <p class="seal"><a href="https://datenschutz-generator.de/" title="Rechtstext von Dr. Schwenke - f&uuml;r weitere Informationen bitte anklicken." target="_blank" rel="noopener noreferrer nofollow"><img src="https://datenschutz-generator.de/wp-content/plugins/ts-dsg/images/dsg-seal/dsg-seal-doc-de.png" alt="Rechtstext von Dr. Schwenke - f&uuml;r weitere Informationen bitte anklicken." width="250" height="250"></a></p>
        </div>
    </section>
    <section id="privacy">
        <div class="text-section">
            <h1>Datenschutzerkl&auml;rung</h1>
            <h2 id="m716">Pr&auml;ambel</h2>
            <p>Mit der folgenden Datenschutzerkl&auml;rung m&ouml;chten wir Sie dar&uuml;ber aufkl&auml;ren, welche Arten Ihrer personenbezogenen Daten (nachfolgend auch kurz als "Daten" bezeichnet) wir zu welchen Zwecken und in welchem Umfang verarbeiten. Die Datenschutzerkl&auml;rung gilt f&uuml;r alle von uns durchgef&uuml;hrten Verarbeitungen personenbezogener Daten, sowohl im Rahmen der Erbringung unserer Leistungen als auch insbesondere auf unseren Webseiten, in mobilen Applikationen sowie innerhalb externer Onlinepr&auml;senzen, wie z. B. unserer Social-Media-Profile (nachfolgend zusammenfassend bezeichnet als "Onlineangebot").</p>
            <p>Die verwendeten Begriffe sind nicht geschlechtsspezifisch.</p>

            <p>Stand: 16. Dezember 2025</p>
            <p class="seal"><a href="https://datenschutz-generator.de/" title="Rechtstext von Dr. Schwenke - f&uuml;r weitere Informationen bitte anklicken." target="_blank" rel="noopener noreferrer nofollow"><img src="https://datenschutz-generator.de/wp-content/plugins/ts-dsg/images/dsg-seal/dsg-seal-pp-de.png" alt="Rechtstext von Dr. Schwenke - f&uuml;r weitere Informationen bitte anklicken." width="250" height="250"></a></p><h2>Inhalts&uuml;bersicht</h2> <ul class="index"><li><a class="index-link" href="#m716">Pr&auml;ambel</a></li><li><a class="index-link" href="#m3">Verantwortlicher</a></li><li><a class="index-link" href="#mOverview">&Uuml;bersicht der Verarbeitungen</a></li><li><a class="index-link" href="#m2427">Ma&szlig;gebliche Rechtsgrundlagen</a></li><li><a class="index-link" href="#m27">Sicherheitsma&szlig;nahmen</a></li><li><a class="index-link" href="#m25">&Uuml;bermittlung von personenbezogenen Daten</a></li><li><a class="index-link" href="#m24">Internationale Datentransfers</a></li><li><a class="index-link" href="#m12">Allgemeine Informationen zur Datenspeicherung und L&ouml;schung</a></li><li><a class="index-link" href="#m10">Rechte der betroffenen Personen</a></li><li><a class="index-link" href="#m225">Bereitstellung des Onlineangebots und Webhosting</a></li><li><a class="index-link" href="#m15">&Auml;nderung und Aktualisierung</a></li><li><a class="index-link" href="#m42">Begriffsdefinitionen</a></li></ul><h2 id="m3">Verantwortlicher</h2><p>Andreas Ha&szlig;ler, Ha&szlig;ler-Schwenk-Weiss GbR<br>Gottlieb-Daimler Stra&szlig;e 11<br>89150 Laichingen</p>
            <p>E-Mail-Adresse: <a href="mailto:info@ahstuckdesign.de">info@ahstuckdesign.de</a></p>

            <h2 id="mOverview">&Uuml;bersicht der Verarbeitungen</h2><p>Die nachfolgende &Uuml;bersicht fasst die Arten der verarbeiteten Daten und die Zwecke ihrer Verarbeitung zusammen und verweist auf die betroffenen Personen.</p><h3>Arten der verarbeiteten Daten</h3>
            <ul><li>Nutzungsdaten.</li><li>Meta-, Kommunikations- und Verfahrensdaten.</li><li>Protokolldaten.</li></ul><h3>Kategorien betroffener Personen</h3><ul><li>Nutzer.</li></ul><h3>Zwecke der Verarbeitung</h3><ul><li>Sicherheitsma&szlig;nahmen.</li><li>Bereitstellung unseres Onlineangebotes und Nutzerfreundlichkeit.</li><li>Informationstechnische Infrastruktur.</li></ul><h2 id="m2427">Ma&szlig;gebliche Rechtsgrundlagen</h2><p><strong>Ma&szlig;gebliche Rechtsgrundlagen nach der DSGVO: </strong>Im Folgenden erhalten Sie eine &Uuml;bersicht der Rechtsgrundlagen der DSGVO, auf deren Basis wir personenbezogene Daten verarbeiten. Bitte nehmen Sie zur Kenntnis, dass neben den Regelungen der DSGVO nationale Datenschutzvorgaben in Ihrem bzw. unserem Wohn- oder Sitzland gelten k&ouml;nnen. Sollten ferner im Einzelfall speziellere Rechtsgrundlagen ma&szlig;geblich sein, teilen wir Ihnen diese in der Datenschutzerkl&auml;rung mit.</p>
            <ul><li><strong>Berechtigte Interessen (Art. 6 Abs. 1 S. 1 lit. f) DSGVO)</strong> - die Verarbeitung ist zur Wahrung der berechtigten Interessen des Verantwortlichen oder eines Dritten notwendig, vorausgesetzt, dass die Interessen, Grundrechte und Grundfreiheiten der betroffenen Person, die den Schutz personenbezogener Daten verlangen, nicht &uuml;berwiegen.</li></ul><p><strong>Nationale Datenschutzregelungen in Deutschland: </strong>Zus&auml;tzlich zu den Datenschutzregelungen der DSGVO gelten nationale Regelungen zum Datenschutz in Deutschland. Hierzu geh&ouml;rt insbesondere das Gesetz zum Schutz vor Missbrauch personenbezogener Daten bei der Datenverarbeitung (Bundesdatenschutzgesetz – BDSG). Das BDSG enth&auml;lt insbesondere Spezialregelungen zum Recht auf Auskunft, zum Recht auf L&ouml;schung, zum Widerspruchsrecht, zur Verarbeitung besonderer Kategorien personenbezogener Daten, zur Verarbeitung f&uuml;r andere Zwecke und zur &Uuml;bermittlung sowie automatisierten Entscheidungsfindung im Einzelfall einschlie&szlig;lich Profiling. Ferner k&ouml;nnen Landesdatenschutzgesetze der einzelnen Bundesl&auml;nder zur Anwendung gelangen.</p>
            <p><strong>Hinweis auf Geltung DSGVO und Schweizer DSG: </strong>Diese Datenschutzhinweise dienen sowohl der Informationserteilung nach dem Schweizer DSG als auch nach der Datenschutzgrundverordnung (DSGVO). Aus diesem Grund bitten wir Sie zu beachten, dass aufgrund der breiteren r&auml;umlichen Anwendung und Verst&auml;ndlichkeit die Begriffe der DSGVO verwendet werden. Insbesondere statt der im Schweizer DSG verwendeten Begriffe „Bearbeitung" von „Personendaten", "&uuml;berwiegendes Interesse" und "besonders sch&uuml;tzenswerte Personendaten" werden die in der DSGVO verwendeten Begriffe „Verarbeitung" von „personenbezogenen Daten" sowie "berechtigtes Interesse" und "besondere Kategorien von Daten" verwendet. Die gesetzliche Bedeutung der Begriffe wird jedoch im Rahmen der Geltung des Schweizer DSG weiterhin nach dem Schweizer DSG bestimmt.</p>

            <h2 id="m27">Sicherheits&shy;ma&szlig;nahmen</h2><p>Wir treffen nach Ma&szlig;gabe der gesetzlichen Vorgaben unter Ber&uuml;cksichtigung des Stands der Technik, der Implementierungskosten und der Art, des Umfangs, der Umst&auml;nde und der Zwecke der Verarbeitung sowie der unterschiedlichen Eintrittswahrscheinlichkeiten und des Ausma&szlig;es der Bedrohung der Rechte und Freiheiten nat&uuml;rlicher Personen geeignete technische und organisatorische Ma&szlig;nahmen, um ein dem Risiko angemessenes Schutzniveau zu gew&auml;hrleisten.</p>
            <p>Zu den Ma&szlig;nahmen geh&ouml;ren insbesondere die Sicherung der Vertraulichkeit, Integrit&auml;t und Verf&uuml;gbarkeit von Daten durch Kontrolle des physischen und elektronischen Zugangs zu den Daten als auch des sie betreffenden Zugriffs, der Eingabe, der Weitergabe, der Sicherung der Verf&uuml;gbarkeit und ihrer Trennung. Des Weiteren haben wir Verfahren eingerichtet, die eine Wahrnehmung von Betroffenenrechten, die L&ouml;schung von Daten und Reaktionen auf die Gef&auml;hrdung der Daten gew&auml;hrleisten. Ferner ber&uuml;cksichtigen wir den Schutz personenbezogener Daten bereits bei der Entwicklung bzw. Auswahl von Hardware, Software sowie Verfahren entsprechend dem Prinzip des Datenschutzes, durch Technikgestaltung und durch datenschutzfreundliche Voreinstellungen.</p>
            <p>Sicherung von Online-Verbindungen durch TLS-/SSL-Verschl&uuml;sselungstechnologie (HTTPS): Um die Daten der Nutzer, die &uuml;ber unsere Online-Dienste &uuml;bertragen werden, vor unerlaubten Zugriffen zu sch&uuml;tzen, setzen wir auf die TLS-/SSL-Verschl&uuml;sselungstechnologie. Secure Sockets Layer (SSL) und Transport Layer Security (TLS) sind die Eckpfeiler der sicheren Daten&uuml;bertragung im Internet. Diese Technologien verschl&uuml;sseln die Informationen, die zwischen der Website oder App und dem Browser des Nutzers (oder zwischen zwei Servern) &uuml;bertragen werden, wodurch die Daten vor unbefugtem Zugriff gesch&uuml;tzt sind. TLS, als die weiterentwickelte und sicherere Version von SSL, gew&auml;hrleistet, dass alle Daten&uuml;bertragungen den h&ouml;chsten Sicherheitsstandards entsprechen. Wenn eine Website durch ein SSL-/TLS-Zertifikat gesichert ist, wird dies durch die Anzeige von HTTPS in der URL signalisiert. Dies dient als ein Indikator f&uuml;r die Nutzer, dass ihre Daten sicher und verschl&uuml;sselt &uuml;bertragen werden.</p>

            <h2 id="m25">&Uuml;bermittlung von personen&shy;bezogenen Daten</h2><p>Im Rahmen unserer Verarbeitung von personenbezogenen Daten kommt es vor, dass diese an andere Stellen, Unternehmen, rechtlich selbstst&auml;ndige Organisationseinheiten oder Personen &uuml;bermittelt beziehungsweise ihnen gegen&uuml;ber offengelegt werden. Zu den Empf&auml;ngern dieser Daten k&ouml;nnen z. B. mit IT-Aufgaben beauftragte Dienstleister geh&ouml;ren oder Anbieter von Diensten und Inhalten, die in eine Website eingebunden sind. In solchen F&auml;llen beachten wir die gesetzlichen Vorgaben und schlie&szlig;en insbesondere entsprechende Vertr&auml;ge bzw. Vereinbarungen, die dem Schutz Ihrer Daten dienen, mit den Empf&auml;ngern Ihrer Daten ab.</p>

            <h2 id="m24">Internationale Datentransfers</h2><p>Datenverarbeitung in Drittl&auml;ndern: Sofern wir Daten in ein Drittland (d. h. au&szlig;erhalb der Europ&auml;ischen Union (EU) oder des Europ&auml;ischen Wirtschaftsraums (EWR)) &uuml;bermitteln oder dies im Rahmen der Nutzung von Diensten Dritter oder der Offenlegung bzw. &Uuml;bermittlung von Daten an andere Personen, Stellen oder Unternehmen geschieht (was erkennbar wird anhand der Postadresse des jeweiligen Anbieters oder wenn in der Datenschutzerkl&auml;rung ausdr&uuml;cklich auf den Datentransfer in Drittl&auml;nder hingewiesen wird), erfolgt dies stets im Einklang mit den gesetzlichen Vorgaben.</p>
            <p>F&uuml;r Daten&uuml;bermittlungen in die USA st&uuml;tzen wir uns vorrangig auf das Data Privacy Framework (DPF), welches durch einen Angemessenheitsbeschluss der EU-Kommission vom 10.07.2023 als sicherer Rechtsrahmen anerkannt wurde. Zus&auml;tzlich haben wir mit den jeweiligen Anbietern Standardvertragsklauseln abgeschlossen, die den Vorgaben der EU-Kommission entsprechen und vertragliche Verpflichtungen zum Schutz Ihrer Daten festlegen.</p>
            <p>Diese zweifache Absicherung gew&auml;hrleistet einen umfassenden Schutz Ihrer Daten: Das DPF bildet die prim&auml;re Schutzebene, w&auml;hrend die Standardvertragsklauseln als zus&auml;tzliche Sicherheit dienen. Sollten sich &Auml;nderungen im Rahmen des DPF ergeben, greifen die Standardvertragsklauseln als zuverl&auml;ssige R&uuml;ckfalloption ein. So stellen wir sicher, dass Ihre Daten auch bei etwaigen politischen oder rechtlichen Ver&auml;nderungen stets angemessen gesch&uuml;tzt bleiben.</p>
            <p>Bei den einzelnen Diensteanbietern informieren wir Sie dar&uuml;ber, ob sie nach dem DPF zertifiziert sind und ob Standardvertragsklauseln vorliegen. Weitere Informationen zum DPF und eine Liste der zertifizierten Unternehmen finden Sie auf der Website des US-Handelsministeriums unter <a href="https://www.dataprivacyframework.gov/" target="_blank">https://www.dataprivacyframework.gov/</a> (in englischer Sprache).</p>
            <p>F&uuml;r Daten&uuml;bermittlungen in andere Drittl&auml;nder gelten entsprechende Sicherheitsma&szlig;nahmen, insbesondere Standardvertragsklauseln, ausdr&uuml;ckliche Einwilligungen oder gesetzlich erforderliche &Uuml;bermittlungen. Informationen zu Drittlandtransfers und geltenden Angemessenheitsbeschl&uuml;ssen k&ouml;nnen Sie dem Informationsangebot der EU-Kommission entnehmen: <a href="https://commission.europa.eu/law/law-topic/data-protection/international-dimension-data-protection_en?prefLang=de" target="_blank">https://commission.europa.eu/law/law-topic/data-protection/international-dimension-data-protection_en?prefLang=de.</a></p>

            <h2 id="m12">Allgemeine Informationen zur Datenspeicherung und L&ouml;schung</h2><p>Wir l&ouml;schen personenbezogene Daten, die wir verarbeiten, gem&auml;&szlig; den gesetzlichen Bestimmungen, sobald die zugrundeliegenden Einwilligungen widerrufen werden oder keine weiteren rechtlichen Grundlagen f&uuml;r die Verarbeitung bestehen. Dies betrifft F&auml;lle, in denen der urspr&uuml;ngliche Verarbeitungszweck entf&auml;llt oder die Daten nicht mehr ben&ouml;tigt werden. Ausnahmen von dieser Regelung bestehen, wenn gesetzliche Pflichten oder besondere Interessen eine l&auml;ngere Aufbewahrung oder Archivierung der Daten erfordern.</p>
            <p>Insbesondere m&uuml;ssen Daten, die aus handels- oder steuerrechtlichen Gr&uuml;nden aufbewahrt werden m&uuml;ssen oder deren Speicherung notwendig ist zur Rechtsverfolgung oder zum Schutz der Rechte anderer nat&uuml;rlicher oder juristischer Personen, entsprechend archiviert werden.</p>
            <p>Unsere Datenschutzhinweise enthalten zus&auml;tzliche Informationen zur Aufbewahrung und L&ouml;schung von Daten, die speziell f&uuml;r bestimmte Verarbeitungsprozesse gelten.</p>
            <p>Bei mehreren Angaben zur Aufbewahrungsdauer oder L&ouml;schungsfristen eines Datums, ist stets die l&auml;ngste Frist ma&szlig;geblich. Daten, die nicht mehr f&uuml;r den urspr&uuml;nglich vorgesehenen Zweck, sondern aufgrund gesetzlicher Vorgaben oder anderer Gr&uuml;nde aufbewahrt werden, verarbeiten wir ausschlie&szlig;lich zu den Gr&uuml;nden, die ihre Aufbewahrung rechtfertigen.</p>
            <p>Aufbewahrung und L&ouml;schung von Daten: Die folgenden allgemeinen Fristen gelten f&uuml;r die Aufbewahrung und Archivierung nach deutschem Recht:</p><ul> <li>10 Jahre - Aufbewahrungsfrist f&uuml;r B&uuml;cher und Aufzeichnungen, Jahresabschl&uuml;sse, Inventare, Lageberichte, Er&ouml;ffnungsbilanz sowie die zu ihrem Verst&auml;ndnis erforderlichen Arbeitsanweisungen und sonstigen Organisationsunterlagen (§ 147 Abs. 1 Nr. 1 i.V.m. Abs. 3 AO, § 14b Abs. 1 UStG, § 257 Abs. 1 Nr. 1 i.V.m. Abs. 4 HGB).</li><li>8 Jahre - Buchungsbelege, wie z. B. Rechnungen und Kostenbelege (§ 147 Abs. 1 Nr. 4 und 4a i.V.m. Abs. 3 Satz 1 AO sowie § 257 Abs. 1 Nr. 4 i.V.m. Abs. 4 HGB).</li><li>6 Jahre - &Uuml;brige Gesch&auml;ftsunterlagen: empfangene Handels- oder Gesch&auml;ftsbriefe, Wiedergaben der abgesandten Handels- oder Gesch&auml;ftsbriefe, sonstige Unterlagen, soweit sie f&uuml;r die Besteuerung von Bedeutung sind, z. B. Stundenlohnzettel, Betriebsabrechnungsb&ouml;gen, Kalkulationsunterlagen, Preisauszeichnungen, aber auch Lohnabrechnungsunterlagen, soweit sie nicht bereits Buchungsbelege sind und Kassenstreifen (§ 147 Abs. 1 Nr. 2, 3, 5 i.V.m. Abs. 3 AO, § 257 Abs. 1 Nr. 2 u. 3 i.V.m. Abs. 4 HGB).</li><li>3 Jahre - Daten, die erforderlich sind, um potenzielle Gew&auml;hrleistungs- und Schadensersatzanspr&uuml;che oder &auml;hnliche vertragliche Anspr&uuml;che und Rechte zu ber&uuml;cksichtigen sowie damit verbundene Anfragen zu bearbeiten, basierend auf fr&uuml;heren Gesch&auml;ftserfahrungen und &uuml;blichen Branchenpraktiken, werden f&uuml;r die Dauer der regul&auml;ren gesetzlichen Verj&auml;hrungsfrist von drei Jahren gespeichert (§§ 195, 199 BGB).</li> </ul>
            <p>Fristbeginn mit Ablauf des Jahres: Beginnt eine Frist nicht ausdr&uuml;cklich zu einem bestimmten Datum und betr&auml;gt sie mindestens ein Jahr, so startet sie automatisch am Ende des Kalenderjahres, in dem das fristausl&ouml;sende Ereignis eingetreten ist. Im Fall laufender Vertragsverh&auml;ltnisse, in deren Rahmen Daten gespeichert werden, ist das fristausl&ouml;sende Ereignis der Zeitpunkt des Wirksamwerdens der K&uuml;ndigung oder sonstige Beendigung des Rechtsverh&auml;ltnisses.</p>

            <h2 id="m10">Rechte der betroffenen Personen</h2><p>Rechte der betroffenen Personen aus der DSGVO: Ihnen stehen als Betroffene nach der DSGVO verschiedene Rechte zu, die sich insbesondere aus Art. 15 bis 21 DSGVO ergeben:</p><ul><li><strong>Widerspruchsrecht: Sie haben das Recht, aus Gr&uuml;nden, die sich aus Ihrer besonderen Situation ergeben, jederzeit gegen die Verarbeitung der Sie betreffenden personenbezogenen Daten, die aufgrund von Art. 6 Abs. 1 lit. e oder f DSGVO erfolgt, Widerspruch einzulegen; dies gilt auch f&uuml;r ein auf diese Bestimmungen gest&uuml;tztes Profiling. Werden die Sie betreffenden personenbezogenen Daten verarbeitet, um Direktwerbung zu betreiben, haben Sie das Recht, jederzeit Widerspruch gegen die Verarbeitung der Sie betreffenden personenbezogenen Daten zum Zwecke derartiger Werbung einzulegen; dies gilt auch f&uuml;r das Profiling, soweit es mit solcher Direktwerbung in Verbindung steht.</strong></li><li><strong>Widerrufsrecht bei Einwilligungen:</strong> Sie haben das Recht, erteilte Einwilligungen jederzeit zu widerrufen.</li><li><strong>Auskunftsrecht:</strong> Sie haben das Recht, eine Best&auml;tigung dar&uuml;ber zu verlangen, ob betreffende Daten verarbeitet werden und auf Auskunft &uuml;ber diese Daten sowie auf weitere Informationen und Kopie der Daten entsprechend den gesetzlichen Vorgaben.</li><li><strong>Recht auf Berichtigung:</strong> Sie haben entsprechend den gesetzlichen Vorgaben das Recht, die Vervollst&auml;ndigung der Sie betreffenden Daten oder die Berichtigung der Sie betreffenden unrichtigen Daten zu verlangen.</li><li><strong>Recht auf L&ouml;schung und Einschr&auml;nkung der Verarbeitung:</strong> Sie haben nach Ma&szlig;gabe der gesetzlichen Vorgaben das Recht, zu verlangen, dass Sie betreffende Daten unverz&uuml;glich gel&ouml;scht werden, bzw. alternativ nach Ma&szlig;gabe der gesetzlichen Vorgaben eine Einschr&auml;nkung der Verarbeitung der Daten zu verlangen.</li><li><strong>Recht auf Daten&uuml;bertragbarkeit:</strong> Sie haben das Recht, Sie betreffende Daten, die Sie uns bereitgestellt haben, nach Ma&szlig;gabe der gesetzlichen Vorgaben in einem strukturierten, g&auml;ngigen und maschinenlesbaren Format zu erhalten oder deren &Uuml;bermittlung an einen anderen Verantwortlichen zu fordern.</li><li><strong>Beschwerde bei Aufsichtsbeh&ouml;rde:</strong> Entsprechend den gesetzlichen Vorgaben und unbeschadet eines anderweitigen verwaltungsrechtlichen oder gerichtlichen Rechtsbehelfs, haben Sie ferner das Recht,  bei einer Datenschutzaufsichtsbeh&ouml;rde, insbesondere einer Aufsichtsbeh&ouml;rde im Mitgliedstaat, in dem Sie sich gew&ouml;hnlich aufhalten, der Aufsichtsbeh&ouml;rde Ihres Arbeitsplatzes oder des Ortes des mutma&szlig;lichen Versto&szlig;es, eine Beschwerde einzulegen, wenn Sie der Ansicht sei sollten, dass die Verarbeitung der Ihre Person betreffenden personenbezogenen Daten gegen die DSGVO verst&ouml;&szlig;t.</li></ul>

            <h2 id="m225">Bereitstellung des Onlineangebots und Webhosting</h2><p>Wir verarbeiten die Daten der Nutzer, um ihnen unsere Online-Dienste zur Verf&uuml;gung stellen zu k&ouml;nnen. Zu diesem Zweck verarbeiten wir die IP-Adresse des Nutzers, die notwendig ist, um die Inhalte und Funktionen unserer Online-Dienste an den Browser oder das Endger&auml;t der Nutzer zu &uuml;bermitteln.</p>
            <ul class="m-elements"><li><strong>Verarbeitete Datenarten:</strong> Nutzungsdaten (z. B. Seitenaufrufe und Verweildauer, Klickpfade, Nutzungsintensit&auml;t und -frequenz, verwendete Ger&auml;tetypen und Betriebssysteme, Interaktionen mit Inhalten und Funktionen); Meta-, Kommunikations- und Verfahrensdaten (z. B. IP-Adressen, Zeitangaben, Identifikationsnummern, beteiligte Personen). Protokolldaten (z. B. Logfiles betreffend Logins oder den Abruf von Daten oder Zugriffszeiten.).</li><li><strong>Betroffene Personen:</strong> Nutzer (z. B. Webseitenbesucher, Nutzer von Onlinediensten).</li><li><strong>Zwecke der Verarbeitung:</strong> Bereitstellung unseres Onlineangebotes und Nutzerfreundlichkeit; Informationstechnische Infrastruktur (Betrieb und Bereitstellung von Informationssystemen und technischen Ger&auml;ten (Computer, Server etc.)). Sicherheitsma&szlig;nahmen.</li><li><strong>Aufbewahrung und L&ouml;schung:</strong> L&ouml;schung entsprechend Angaben im Abschnitt "Allgemeine Informationen zur Datenspeicherung und L&ouml;schung".</li><li class=""><strong>Rechtsgrundlagen:</strong> Berechtigte Interessen (Art. 6 Abs. 1 S. 1 lit. f) DSGVO).</li></ul><p><strong>Weitere Hinweise zu Verarbeitungsprozessen, Verfahren und Diensten:</strong></p><ul class="m-elements"><li><strong>Bereitstellung Onlineangebot auf gemietetem Speicherplatz: </strong>F&uuml;r die Bereitstellung unseres Onlineangebotes nutzen wir Speicherplatz, Rechenkapazit&auml;t und Software, die wir von einem entsprechenden Serveranbieter (auch "Webhoster" genannt) mieten oder anderweitig beziehen; <span class=""><strong>Rechtsgrundlagen:</strong> Berechtigte Interessen (Art. 6 Abs. 1 S. 1 lit. f) DSGVO).</span></li><li><strong>Erhebung von Zugriffsdaten und Logfiles: </strong>Der Zugriff auf unser Onlineangebot wird in Form von sogenannten "Server-Logfiles" protokolliert. Zu den Serverlogfiles k&ouml;nnen die Adresse und der Name der abgerufenen Webseiten und Dateien, Datum und Uhrzeit des Abrufs, &uuml;bertragene Datenmengen, Meldung &uuml;ber erfolgreichen Abruf, Browsertyp nebst Version, das Betriebssystem des Nutzers, Referrer URL (die zuvor besuchte Seite) und im Regelfall IP-Adressen und der anfragende Provider geh&ouml;ren. Die Serverlogfiles k&ouml;nnen zum einen zu Sicherheitszwecken eingesetzt werden, z. B. um eine &Uuml;berlastung der Server zu vermeiden (insbesondere im Fall von missbr&auml;uchlichen Angriffen, sogenannten DDoS-Attacken), und zum anderen, um die Auslastung der Server und ihre Stabilit&auml;t sicherzustellen; <span class=""><strong>Rechtsgrundlagen:</strong> Berechtigte Interessen (Art. 6 Abs. 1 S. 1 lit. f) DSGVO). </span><strong>L&ouml;schung von Daten:</strong> Logfile-Informationen werden f&uuml;r die Dauer von maximal 30 Tagen gespeichert und danach gel&ouml;scht oder anonymisiert. Daten, deren weitere Aufbewahrung zu Beweiszwecken erforderlich ist, sind bis zur endg&uuml;ltigen Kl&auml;rung des jeweiligen Vorfalls von der L&ouml;schung ausgenommen.</li><li><strong>Vercel Inc.: </strong>Leistungen auf dem Gebiet der Bereitstellung von informationstechnischer Infrastruktur und verbundenen Dienstleistungen (z. B. Speicherplatz und/oder Rechenkapazit&auml;ten); Rechtsgrundlagen: Berechtigte Interessen (Art. 6 Abs. 1 S. 1 lit. f) DSGVO); Auftragsverarbeitungsvertrag: Wird vom Dienstanbieter bereitgestellt; <strong>Dienstanbieter:</strong> c/o EDPO, Avenue Huart Hamoir 71, 1030 Brussels, Belgium; <strong>Website:</strong> <a href="https://vercel.com/" target="_blank">https://vercel.com/</a>. <strong>Datenschutzerkl&auml;rung:</strong> <a href="https://vercel.com/legal/privacy-policy" target="_blank">https://vercel.com/legal/privacy-policy</a>.</li></ul>
            <h2 id="m15">&Auml;nderung und Aktualisierung</h2><p>Wir bitten Sie, sich regelm&auml;&szlig;ig &uuml;ber den Inhalt unserer Datenschutzerkl&auml;rung zu informieren. Wir passen die Datenschutzerkl&auml;rung an, sobald die &Auml;nderungen der von uns durchgef&uuml;hrten Datenverarbeitungen dies erforderlich machen. Wir informieren Sie, sobald durch die &Auml;nderungen eine Mitwirkungshandlung Ihrerseits (z. B. Einwilligung) oder eine sonstige individuelle Benachrichtigung erforderlich wird.</p>
            <p>Sofern wir in dieser Datenschutzerkl&auml;rung Adressen und Kontaktinformationen von Unternehmen und Organisationen angeben, bitten wir zu beachten, dass die Adressen sich &uuml;ber die Zeit &auml;ndern k&ouml;nnen und bitten die Angaben vor Kontaktaufnahme zu pr&uuml;fen.</p>

            <h2 id="m42">Begriffs&shy;definitionen</h2><p>In diesem Abschnitt erhalten Sie eine &Uuml;bersicht &uuml;ber die in dieser Datenschutzerkl&auml;rung verwendeten Begrifflichkeiten. Soweit die Begrifflichkeiten gesetzlich definiert sind, gelten deren gesetzliche Definitionen. Die nachfolgenden Erl&auml;uterungen sollen dagegen vor allem dem Verst&auml;ndnis dienen.</p>
            <ul class="glossary"><li><strong>Meta-, Kommunikations- und Verfahrensdaten:</strong> Meta-, Kommunikations- und Verfahrensdaten sind Kategorien, die Informationen &uuml;ber die Art und Weise enthalten, wie Daten verarbeitet, &uuml;bermittelt und verwaltet werden. Meta-Daten, auch bekannt als Daten &uuml;ber Daten, umfassen Informationen, die den Kontext, die Herkunft und die Struktur anderer Daten beschreiben. Sie k&ouml;nnen Angaben zur Dateigr&ouml;&szlig;e, dem Erstellungsdatum, dem Autor eines Dokuments und den &Auml;nderungshistorien beinhalten. Kommunikationsdaten erfassen den Austausch von Informationen zwischen Nutzern &uuml;ber verschiedene Kan&auml;le, wie E-Mail-Verkehr, Anrufprotokolle, Nachrichten in sozialen Netzwerken und Chat-Verl&auml;ufe, inklusive der beteiligten Personen, Zeitstempel und &Uuml;bertragungswege. Verfahrensdaten beschreiben die Prozesse und Abl&auml;ufe innerhalb von Systemen oder Organisationen, einschlie&szlig;lich Workflow-Dokumentationen, Protokolle von Transaktionen und Aktivit&auml;ten, sowie Audit-Logs, die zur Nachverfolgung und &Uuml;berpr&uuml;fung von Vorg&auml;ngen verwendet werden. </li><li><strong>Nutzungsdaten:</strong> Nutzungsdaten beziehen sich auf Informationen, die erfassen, wie Nutzer mit digitalen Produkten, Dienstleistungen oder Plattformen interagieren. Diese Daten umfassen eine breite Palette von Informationen, die aufzeigen, wie Nutzer Anwendungen nutzen, welche Funktionen sie bevorzugen, wie lange sie auf bestimmten Seiten verweilen und &uuml;ber welche Pfade sie durch eine Anwendung navigieren. Nutzungsdaten k&ouml;nnen auch die H&auml;ufigkeit der Nutzung, Zeitstempel von Aktivit&auml;ten, IP-Adressen, Ger&auml;teinformationen und Standortdaten einschlie&szlig;en. Sie sind besonders wertvoll f&uuml;r die Analyse des Nutzerverhaltens, die Optimierung von Benutzererfahrungen, das Personalisieren von Inhalten und das Verbessern von Produkten oder Dienstleistungen. Dar&uuml;ber hinaus spielen Nutzungsdaten eine entscheidende Rolle beim Erkennen von Trends, Vorlieben und m&ouml;glichen Problembereichen innerhalb digitaler Angebote </li><li><strong>Personenbezogene Daten:</strong> "Personenbezogene Daten" sind alle Informationen, die sich auf eine identifizierte oder identifizierbare nat&uuml;rliche Person (im Folgenden "betroffene Person") beziehen; als identifizierbar wird eine nat&uuml;rliche Person angesehen, die direkt oder indirekt, insbesondere mittels Zuordnung zu einer Kennung wie einem Namen, zu einer Kennnummer, zu Standortdaten, zu einer Online-Kennung (z. B. Cookie) oder zu einem oder mehreren besonderen Merkmalen identifiziert werden kann, die Ausdruck der physischen, physiologischen, genetischen, psychischen, wirtschaftlichen, kulturellen oder sozialen Identit&auml;t dieser nat&uuml;rlichen Person sind. </li><li><strong>Protokolldaten:</strong> Protokolldaten sind Informationen &uuml;ber Ereignisse oder Aktivit&auml;ten, die in einem System oder Netzwerk protokolliert wurden. Diese Daten enthalten typischerweise Informationen wie Zeitstempel, IP-Adressen, Benutzeraktionen, Fehlermeldungen und andere Details &uuml;ber die Nutzung oder den Betrieb eines Systems. Protokolldaten werden oft zur Analyse von Systemproblemen, zur Sicherheits&uuml;berwachung oder zur Erstellung von Leistungsberichten verwendet. </li><li><strong>Verantwortlicher:</strong> Als "Verantwortlicher" wird die nat&uuml;rliche oder juristische Person, Beh&ouml;rde, Einrichtung oder andere Stelle, die allein oder gemeinsam mit anderen &uuml;ber die Zwecke und Mittel der Verarbeitung von personenbezogenen Daten entscheidet, bezeichnet. </li><li><strong>Verarbeitung:</strong> "Verarbeitung" ist jeder mit oder ohne Hilfe automatisierter Verfahren ausgef&uuml;hrte Vorgang oder jede solche Vorgangsreihe im Zusammenhang mit personenbezogenen Daten. Der Begriff reicht weit und umfasst praktisch jeden Umgang mit Daten, sei es das Erheben, das Auswerten, das Speichern, das &Uuml;bermitteln oder das L&ouml;schen. </li></ul>
        </div>
    </section>
</main>

<style>
  section#hero {
    width: 100%;
    height: 100vh;

    margin: 0;

    .logo {
      position: absolute;
      top: var(--gutter-width);
      left: var(--gutter-width);

      @media(min-width: 1200px) {
        width: 10vw;
      }
    }

    video.section--background {
      width: 100%;
      height: 100%;
      object-position: center;
      object-fit: cover;
    }

    #logo-large {
      position: absolute;
      bottom: calc(var(--logo-bottom) * 1.7);
      left: var(--gutter-width);

      max-width: 80vw;

      @media(min-width: 1200px) {
        bottom: calc(var(--logo-bottom));
      }

      path {
        fill: url(#image);
      }
    }
  }

    .text-section {
      grid-column: 1/4;

      @media (min-width: 1200px) {
        grid-column: 2/5;
      }

      @media (min-width: 2400px) {
        grid-column: 2/5;
      }

      * {
        word-wrap: break-word;
        word-break: auto-phrase;
      }

      :global(h2) {
        font-size: var(--font-size-h2);
        font-family: var(--font-family-semibold);
        font-weight: 400;
        font-style: normal;
        line-height: 1em;
        color: inherit;
        text-transform: uppercase;
        margin-top: 1em;
        margin-bottom: 0.7em;
      }
    }
</style>