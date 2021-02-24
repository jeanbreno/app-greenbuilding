# app-greenbuilding
Sistema gerado para entrega final do projeto da matéria Algoritmos e Lógica de programação. 


#include <stdio.h>
#include <stdlib.h>
#include <locale.h>
#include <math.h>

// NR - 24, NR - 15, NR - 16
float fTrabalhoExterno ();
float fShopping ();
float fTransporte ();
float fGeral ();
float fLograPublico ();
float insalubridade ();
float periculosidade ();

// Loja Online
float venda ();

// Cálculo de Pintura
float pintura ();

// Cálculo de Ar-Condicionado
float arcondicionado ();

// Cálculo de Piso
float piso ();

// Cálculo de Tijolos
float tijolo ();
float seisFuros();
float oitoFuros();
float noveFuros();



int main() 
{
	
	setlocale(LC_ALL, "");
	int trabalhoExterno, segmento, lograPublico, opcoes;
	
	printf("\n----------------------------------------------------------------------------");
	printf("\n----------------------------------------------------------------------------");
	printf("\n-------------------------- APP GREEN BUILDING-------------------------------");
	printf("\n----------------------------------------------------------------------------");
	printf("\n----------------------------------------------------------------------------\n");

	printf("\n\n [1] NR 24 - Condições Sanitárias e de Conforto nos Locais de Trabalho");
	printf("\n\n [2] NR 15 - Atividades e operações insalubres");
	printf("\n\n [3] NR 16 - Atividades e operações perigosas");
	printf("\n\n [4] Cálculo - Pintura");
	printf("\n\n [5] Cálculo - Ar-Condicionado");
	printf("\n\n [6] Cálculo - Tijolo");
	printf("\n\n [7] Cálculo - Piso");
	printf("\n\n [8] Loja Online");
	printf("\n\n [9] Sair\n\n");

	printf("\n\n\t Escolha: ");	
		scanf("\t%d", &opcoes);
		while (opcoes <1 || opcoes > 8)
						{
							printf("\n\t Opção inválida! ");
							printf("\n\t Digite a sua escolha novamente ");
							printf("\n\t Escolha: \t");
								scanf("\t%d", &opcoes);
						}
	 
	 
				switch (opcoes)
				{
					case 1:
						printf("\n\n\t Esta norma estabelece as condições mínimas de higiene e de conforto a serem");
						printf("\n\t observadas pelas organizações.");
						printf("\n\n Seu colaborador está em trabalho externo de prestação de serviços? \n");
						printf("\n\t [1] Sim \n\t [2] Não");
						printf("\n\t Escolha: \t");
							scanf("\t%d", &trabalhoExterno);
							while (trabalhoExterno != 1 && trabalhoExterno != 2)
								{
									printf("\n\t Opção inválida! ");
									printf("\n\t Digite novamente ");
									printf("\n\n\t [1] Sim \n\t [2] Não");
									printf("\n\t Escolha: \t");
										scanf("\t%d", &trabalhoExterno);
								}
							
							if (trabalhoExterno == 1)
							{
								printf("\n O trabalho externo é em logradouro público? \n");
								printf("\n\t [1] Sim \n\t [2] Não");
								printf("\n\t Escolha: \t");
									scanf("\t%d", &lograPublico);
									while (lograPublico != 1 && lograPublico != 2)
										{
											printf("\n\t Opção inválida! ");
											printf("\n\t Digite novamente ");
											printf("\n\n\t [1] Sim \n\t [2] Não");
											printf("\n\t Escolha: \t");
												scanf("\t%d", &lograPublico);
										}
										if (lograPublico == 1)
										{
											fLograPublico (); // chamar função logradouro publico
										}
										else if (lograPublico == 2)
											{
												fTrabalhoExterno (); // chamar função do trabalho externo
											}
							}
							else if (trabalhoExterno == 2)
								{
									// continuar programa 
								
									printf("\n Qual o segmento da sua empresa? \n");
									printf("\n\t [1] Shopping Center \n\t [2] Transporte público rodoviário coletivo urbano de passageiros em atividade externa \n\t [3] Outros  ");
									printf("\n\t Escolha: \t");
										scanf("\t%d", &segmento);
										while (segmento != 1 && segmento != 2 && segmento != 3)
											{
												printf("\n\t Opção inválida! ");
												printf("\n\t Digite novamente ");
												printf("\n\n\t [1] Shopping Center \n\t [2] Transporte público rodoviário coletivo urbano de passageiros em atividade externa \n\t [3] Outros  ");
												printf("\n\t Escolha: \t");
													scanf("\t%d", &segmento);
											}
												if (segmento == 1)
													{
														fShopping (); // chamar função do shopping center
													}
												else if(segmento == 2)
													{
														fTransporte (); // chamar função transporte público
													} 
													else if(segmento == 3)
														{
															fGeral (); // chamar função geral
														} ;
								}
					break;
					case 2:
						insalubridade ();
					break;
					case 3:
						periculosidade ();
					break;
					case 4:
						pintura ();
					break;
					case 5:
						arcondicionado ();
					break;
					case 6:
						tijolo ();
					break;
					case 7:
						piso ();
					break;
					case 8:
						venda ();
					break;
					case 9:
						system ("pause");
						return 0;			}
	
	
}

float fTrabalhoExterno ()
{
	int retorno;
	printf("\n\n\n\t Anexo II da NR 24");
	printf("\n\n 1. Para efeito deste Anexo, considera-se trabalho externo todo aquele realizado fora do estabelecimento");
	printf("\n do empregador cuja execução se dará no estabelicmento do cliente ou em logradouro público.");
	printf("\n\n 2. Nas atividades desenvolvidas em estabelecimento do cliente, este será o responsável pelas garantias ");
	printf("\n de conforto para satisfação das necessidades básicas de higiene e alimentação, conforme item 24.1 da NR 24.");
	printf("\n\n 3. O uso de intalações sanitárias em trabalhos externos deve ser gratuito para o trabalhador.");
	printf("\n\n 4. Aos trabalhadores, em trabalho externo que levam suas próprias refeições, devem ser oferecidos dispositivos ");
	printf("\n térmicos para conservação e aquecimento dos alimentos.");
	printf("\n\n 5. Em trabalhos externos o atendimento a este Anexo poderá ocorrer mediante convênio com estabelecimento nas ");
	printf("\n proximidades do local do trabalho, garantido o transporte de todos os trabalhadores até o referido local. \n\n");
	printf("\n\n\t Deseja realizar outra consulta? ");
	printf("\n\t [1] Sim \n\t [2] Não")	;
	printf("\n\t Escolha:  ");
		scanf("\t %d", &retorno );
		while (retorno <1 || retorno >2 )
		{
				printf("\n\t Opção inválida! ");
				printf("\n\t Digite novamente ");
				printf("\n\n\t [1] Sim \n\t [2] Não");
				printf("\n\t Escolha: \t");
				scanf("\t %d", &retorno );
		}
			if (retorno == 1)
			{
				system("cls");
				return main ();
			}
			else printf("\n\n\tObrigado! Até mais...\n");
}

float fLograPublico ()
{ 
	int trabalhadores, retorno;
	printf("\n\n Quantidade de trabalhadores em logradouro público (limite de 200): ");
		scanf("\t%d", &trabalhadores);
		while (trabalhadores > 200)
				{
					printf("\n\t Opa! Nosso sistema, por enquanto, só faz o cálculo com limite de 200 funcionários. ");
					printf("\n\t Digite novamente ");
					printf("\n\n Quantidade de trabalhadores em logradouro público (limite de 200): ");
						scanf("\t%d", &trabalhadores);
				}
				if (trabalhadores <= 20)
				{
					printf("\n\t Requer uma instalação sanitária composta por bacia sanitária e lavatório.");
				}
				else if (trabalhadores <=40) 
					{
						printf("\n\t Requer duas instalações sanitárias compostas por bacias sanitárias e lavatórios.");
					}
					else if (trabalhadores <=60) 
						{
							printf("\n\t Requer três instalações sanitárias compostas por bacias sanitárias e lavatórios.");
						}
						else if (trabalhadores <=80) 
							{
								printf("\n\t Requer quatro instalações sanitárias compostas por bacias sanitárias e lavatórios.");
							}
							else if (trabalhadores <=100) 
								{
									printf("\n\t Requer cinco instalações sanitárias compostas por bacias sanitárias e lavatórios.");
								}
								else if (trabalhadores <=120) 
									{
										printf("\n\t Requer seis instalações sanitárias compostas por bacias sanitárias e lavatórios.");
									}
									else if (trabalhadores <=140) 
										{
											printf("\n\t Requer sete instalações sanitárias compostas por bacias sanitárias e lavatórios.");
										}
										else if (trabalhadores <=160) 
											{
												printf("\n\t Requer oito instalações sanitárias compostas por bacias sanitárias e lavatórios.");
											}
											else if (trabalhadores <=180) 
												{
													printf("\n\t Requer nove instalações sanitárias compostas por bacias sanitárias e lavatórios.");
												}
												else if (trabalhadores <=200) 
													{
														printf("\n\t Requer dez instalações sanitárias compostas por bacias sanitárias e lavatórios.");
													}
					
					
	printf("\n\n\n\t Anexo II da NR 24");
	printf("\n\n 1. Para efeito deste Anexo, considera-se trabalho externo todo aquele realizado fora do estabelecimento");
	printf("\n do empregador cuja execução se dará no estabelicmento do cliente ou em logradouro público.");
	printf("\n\n 2. Nas atividades desenvolvidas em estabelecimento do cliente, este será o responsável pelas garantias ");
	printf("\n de conforto para satisfação das necessidades básicas de higiene e alimentação, conforme item 24.1 da NR 24.");
	printf("\n\n 2.1 Sempre que o trabalho externo, móvel ou temporário, ocorrer preponderantemente em logradouro público, ");
	printf("\n em frente de trabalho, deverá ser garantido pelo empregador: ");
	printf("\n\n\t a) instalações sanitárias compostas de bacia sanitária e lavatório para cada grupo de 20 (vinte) ");
	printf("\n\t trabalhadores ou fração, podendo ser usados banheiros químicos dotados de mecanismo de descarga ou  ");
	printf("\n\t de isolamento dos dejetos, com respiro e ventilação, material para lavagem e enxugo das mãos, sendo  ");
	printf("\n\t proibido o uso de toalhas coletivas, garantida a higienização diária dos módulos;");
	printf("\n\n\t b) local para refeição protegido contra intempéries e em condições de higiene, que atenda a  ");
	printf("\n\t todos os trabalhadores ou prover meio de custeio para alimentação em estabelecimentos comerciais; e");
	printf("\n\n\t c) água fresca e potável acondicionada em recipientes térmicos em bom estado de conservação e em ");
	printf("\n\t quantidade suficiente.");
	printf("\n\n 3. O uso de intalações sanitárias em trabalhos externos deve ser gratuito para o trabalhador.");
	printf("\n\n 4. Aos trabalhadores, em trabalho externo que levam suas próprias refeições, devem ser oferecidos dispositivos ");
	printf("\n térmicos para conservação e aquecimento dos alimentos.");
	printf("\n\n 5. Em trabalhos externos o atendimento a este Anexo poderá ocorrer mediante convênio com estabelecimento nas ");
	printf("\n proximidades do local do trabalho, garantido o transporte de todos os trabalhadores até o referido local. \n\n");
	
	printf("\n\n\t Deseja realizar outra consulta? ");
	printf("\n\t [1] Sim \n\t [2] Não")	;
	printf("\n\t Escolha:  ");
		scanf("\t %d", &retorno );
		while (retorno <1 || retorno >2 )
		{
				printf("\n\t Opção inválida! ");
				printf("\n\t Digite novamente ");
				printf("\n\n\t [1] Sim \n\t [2] Não");
				printf("\n\t Escolha: \t");
				scanf("\t %d", &retorno );
		}
		if (retorno == 1)
		{
			system("cls");
			return main ();
		}
		else printf("\n\n\tObrigado! Até mais...\n");
}

float fShopping ()
{
	int insalubre, trabalhadores, retorno;
	printf("\n\n Seu colaborador exerce uma atividade com exposição a material infectante, substâncias tôxicas, ");
	printf("\n irritantes ou que provoquem sujidade? ");
	printf("\n\n\t [1] Sim \n\t [2] Não");
	printf("\n\t Escolha: \t");
		scanf("\t%d", &insalubre);
		while (insalubre != 1 && insalubre != 2)
				{
					printf("\n\t Opção inválida! ");
					printf("\n\t Digite novamente ");
					printf("\n\n\t [1] Sim \n\t [2] Não");
					printf("\n\t Escolha: \t");
						scanf("\t%d", &insalubre);
				}
		
		if (insalubre == 1)
		{
			printf("\n\n\t Digite a quantidade de trabalhadores nessa posição (Limite de 100): ");
				scanf("\t%d", &trabalhadores);
				while (trabalhadores > 100)
					{
						printf("\n\t Que pena! Só conseguimos calcular até 100 trabalhadores. ");
						printf("\n\t Digite novamente ");
						printf("\n\n\t Digite a quantidade de trabalhadores nessa posição (Limite de 100): ");
							scanf("\t%d", &trabalhadores);
					}
					if (trabalhadores <= 10)
						{
							printf("\n\t Requer uma instalação sanitária composta por bacia sanitária e lavatório,");
							printf("\n\t um vestiário e um chuveiro, separados por sexo.");
						}
						else if (trabalhadores <=20) 
							{
								printf("\n\t Requer duas instalações sanitárias compostas por bacia sanitária e lavatório,");
								printf("\n\t dois vestiários e dois chuveiros, separados por sexo.");
							}
							else if (trabalhadores <=30) 
								{
									printf("\n\t Requer três instalações sanitárias compostas por bacia sanitária e lavatório,");
									printf("\n\t três vestiários e três chuveiros, separados por sexo.");						
								}
								else if (trabalhadores <=40) 
									{
										printf("\n\t Requer quatro instalações sanitárias compostas por bacia sanitária e lavatório,");
										printf("\n\t quatro vestiários e quatro chuveiros, separados por sexo.");
									}
									else if (trabalhadores <=50) 
										{
											printf("\n\t Requer cinco instalações sanitárias compostas por bacia sanitária e lavatório,");
											printf("\n\t cinco vestiários e cinco chuveiros, separados por sexo.");
										}
										else if (trabalhadores <=60) 
											{
												printf("\n\t Requer seis instalações sanitárias compostas por bacia sanitária e lavatório,");
												printf("\n\t seis vestiários e seis chuveiros, separados por sexo.");
											}
											else if (trabalhadores <=70) 
												{
													printf("\n\t Requer sete instalações sanitárias compostas por bacia sanitária e lavatório,");
													printf("\n\t sete vestiários e sete chuveiros, separados por sexo.");
												}
												else if (trabalhadores <=80) 
													{
														printf("\n\t Requer oito instalações sanitárias compostas por bacia sanitária e lavatório,");
														printf("\n\t oito vestiários e oito chuveiros, separados por sexo.");
													}
													else if (trabalhadores <=90) 
														{
															printf("\n\t Requer nove instalações sanitárias compostas por bacia sanitária e lavatório,");
															printf("\n\t nove vestiários e nove chuveiros, separados por sexo.");
														}
														else if (trabalhadores <=100) 
															{
																printf("\n\t Requer dez instalações sanitárias compostas por bacia sanitária e lavatório,");
																printf("\n\t dez vestiários e dez chuveiros, separados por sexo.");
															} 
														
		}
		else if (insalubre == 2)
			{
				printf("\n\n\t Digite a quantidade de trabalhadores nessa posição (Limite de 200): ");
				scanf("\t%d", &trabalhadores);
				while (trabalhadores > 200)
					{
						printf("\n\t Opção inválida! Lembre-se do limite de até 200 colaboradores. ");
						printf("\n\t Digite novamente ");
						printf("\n\n\t Digite a quantidade de trabalhadores nessa posição (Limite de 200): ");
							scanf("\t%d", &trabalhadores);
					}
					if (trabalhadores <= 20)
						{
							printf("\n\t Requer uma instalação sanitária composta por bacia sanitária e lavatório,");
							printf("\n\t um vestiário e um chuveiro, separados por sexo.");
						}
						else if (trabalhadores <=40) 
							{
								printf("\n\t Requer duas instalações sanitárias compostas por bacia sanitária e lavatório,");
								printf("\n\t dois vestiários e dois chuveiros, separados por sexo.");
							}
							else if (trabalhadores <=60) 
								{
									printf("\n\t Requer três instalações sanitárias compostas por bacia sanitária e lavatório,");
									printf("\n\t três vestiários e três chuveiros, separados por sexo.");						
								}
								else if (trabalhadores <=80) 
									{
										printf("\n\t Requer quatro instalações sanitárias compostas por bacia sanitária e lavatório,");
										printf("\n\t quatro vestiários e quatro chuveiros, separados por sexo.");
									}
									else if (trabalhadores <=100) 
										{
											printf("\n\t Requer cinco instalações sanitárias compostas por bacia sanitária e lavatório,");
											printf("\n\t cinco vestiários e cinco chuveiros, separados por sexo.");
										}
										else if (trabalhadores <=120) 
											{
												printf("\n\t Requer seis instalações sanitárias compostas por bacia sanitária e lavatório,");
												printf("\n\t seis vestiários e seis chuveiros, separados por sexo.");
											}
											else if (trabalhadores <=140) 
												{
													printf("\n\t Requer sete instalações sanitárias compostas por bacia sanitária e lavatório,");
													printf("\n\t sete vestiários e sete chuveiros, separados por sexo.");
												}
												else if (trabalhadores <=160) 
													{
														printf("\n\t Requer oito instalações sanitárias compostas por bacia sanitária e lavatório,");
														printf("\n\t oito vestiários e oito chuveiros, separados por sexo.");
													}
													else if (trabalhadores <=180) 
														{
															printf("\n\t Requer nove instalações sanitárias compostas por bacia sanitária e lavatório,");
															printf("\n\t nove vestiários e nove chuveiros, separados por sexo.");
														}
														else if (trabalhadores <=200) 
															{
																printf("\n\t Requer dez instalações sanitárias compostas por bacia sanitária e lavatório,");
																printf("\n\t dez vestiários e dez chuveiros, separados por sexo.");
															} 
			}
			
	printf("\n\n\n\t Anexo I da NR 24");
	printf("\n\n\t 1. Para efeito deste Anexo, considera-se Shopping Center o espaço planejado sob uma administração central" );
	printf("\n\t sujeito a normas contratuais padronizadas, procurando assegurar convivência integrada, composto por ");
	printf("\n\t estabelecimentos tais como: lojas de qualquer natureza e quiosques, lanchonetes, restaurantes, salas de ");
	printf("\n\t cinema e estacionamento, destinados à exploração comercial e à prestação de serviços.");
	printf("\n\n\t 2. A administração central é responsável pela disponibilização das instalações sanitárias, vestiários e"); 
	printf("\n\t ambientes para refeições aos seus trabalhadores e aos trabalhadores dos estabelecimentos que não disponham");
	printf("\n\t de espaço construtivo para atender os dispositivos desta NR em seus estabelecimentos.");
	printf("\n\n\t\t 2.1 A administração central disponibilizará local para conservação, aquecimento da alimentação trazida pelos"); 
	printf("\n\t\t trabalhadores, bem como para tomada das refeições.");
	printf("\n\n\t\t 2.2 A administração central disponibilizará vestiário para troca de roupa dos trabalhadores usuários, dos ");
	printf("\n\t\t quais são exigidos o uso de uniforme e vestimentas de trabalho, bem como para guarda de seus pertences.");
	printf("\n\n\n\t 3. Os estabelecimentos referidos no item 1 ficam dispensados dos itens relativos a instalações sanitárias, ");
	printf("\n\t vestiários e locais para refeições, desde que os trabalhadores possam utilizar as instalações sanitárias e ");
	printf("\n\t a praça de alimentação do Shopping Center ou outro espaço destinado a estes fins, conforme o estabelecido ");
	printf("\n\t nesta norma.");
	printf("\n\n\t 4. Aos trabalhadores de lanchonetes, restaurantes ou similares deverão ser disponibilizados vestiários");
	printf("\n\t e instalações sanitárias com chuveiros na proporção de um conjunto para cada grupo de 20 (vinte) trabalhadores");
	printf("\n\t ou fração, obedecendo ao horário do turno de maior contingente.");
	printf("\n\n\t\t 4.1 Aos trabalhadores de atividades com exposição a material infectante, substâncias tóxicas, irritantes ou ");
	printf("\n\t\t que provoquem sujidade deverão ser disponibilizados vestiários e instalações sanitárias com chuveiros na ");
	printf("\n\t\t proporção de um conjunto para cada grupo de 10 (dez) trabalhadores ou fração, obedecendo ao horário do ");
	printf("\n\t\t turno de maior contingente. \n\n\n");
			
			
	printf("\n\n\t Deseja realizar outra consulta? ");
	printf("\n\t [1] Sim \n\t [2] Não")	;
	printf("\n\t Escolha:  ");
		scanf("\t %d", &retorno );
		while (retorno <1 || retorno >2 )
		{
				printf("\n\t Opção inválida! ");
				printf("\n\t Digite novamente ");
				printf("\n\n\t [1] Sim \n\t [2] Não");
				printf("\n\t Escolha: \t");
				scanf("\t %d", &retorno );
		}
		if (retorno == 1)
		{
			system("cls");
			return main ();
		}
		else printf("\n\n\tObrigado! Até mais...\n");														
		
}

float fTransporte ()
{
	int trabalhadores, retorno;
	printf("\n\n\t Digite a quantidade de trabalhadores em transporte público urbano (Limite de 200): ");
	scanf("\t%d", &trabalhadores);
		while (trabalhadores > 200)
			{
				printf("\n\t Opção inválida! Lembre-se do limite de até 200 colaboradores. ");
				printf("\n\t Digite novamente ");
				printf("\n\n\t Digite a quantidade de trabalhadores nessa posição (Limite de 200): ");
					scanf("\t%d", &trabalhadores);
			}
			if (trabalhadores <= 20)
				{
					printf("\n\t Requer uma instalação sanitária composta por bacia sanitária e lavatório,");
					printf("\n\t separada por sexo.");
				}
				else if (trabalhadores <=40) 
					{
						printf("\n\t Requer duas instalações sanitárias compostas por bacia sanitária e lavatório,");
						printf("\n\t separadas por sexo.");
					}
					else if (trabalhadores <=60) 
						{
							printf("\n\t Requer três instalações sanitárias compostas por bacia sanitária e lavatório,");
							printf("\n\t separadas por sexo.");						
						}
						else if (trabalhadores <=80) 
							{
								printf("\n\t Requer quatro instalações sanitárias compostas por bacia sanitária e lavatório,");
								printf("\n\t separadas por sexo.");
							}
							else if (trabalhadores <=100) 
								{
									printf("\n\t Requer cinco instalações sanitárias compostas por bacia sanitária e lavatório,");
									printf("\n\t separadas por sexo.");
								}
								else if (trabalhadores <=120) 
									{
										printf("\n\t Requer seis instalações sanitárias compostas por bacia sanitária e lavatório,");
										printf("\n\t separadas por sexo.");
									}
									else if (trabalhadores <=140) 
										{
											printf("\n\t Requer sete instalações sanitárias compostas por bacia sanitária e lavatório,");
											printf("\n\t separadas por sexo.");
										}
										else if (trabalhadores <=160) 
											{
												printf("\n\t Requer oito instalações sanitárias compostas por bacia sanitária e lavatório,");
												printf("\n\t separadas por sexo.");
											}
											else if (trabalhadores <=180) 
												{
													printf("\n\t Requer nove instalações sanitárias compostas por bacia sanitária e lavatório,");
													printf("\n\t separadas por sexo.");
												}
												else if (trabalhadores <=200) 
													{
														printf("\n\t Requer dez instalações sanitárias compostas por bacia sanitária e lavatório,");
														printf("\n\t separadas por sexo.");
													}
		printf("\n\n\t Deseja realizar outra consulta? ");
		printf("\n\t [1] Sim \n\t [2] Não")	;
		printf("\n\t Escolha:  ");
			scanf("\t %d", &retorno );
			while (retorno <1 || retorno >2 )
			{
					printf("\n\t Opção inválida! ");
					printf("\n\t Digite novamente ");
					printf("\n\n\t [1] Sim \n\t [2] Não");
					printf("\n\t Escolha: \t");
					scanf("\t %d", &retorno );
			}
				if (retorno == 1)
				{
					system("cls");
					return main ();
				}
				else printf("\n\n\tObrigado! Até mais...\n");
}

float fGeral ()
{
	int op, retorno ;
	float areaMin, trabalhadores;
	
	 
		printf("\n\n\t Sobre qual item você quer informação? ");
		printf("\n\n\t\t [1] Instalações sanitárias ");
		printf("\n\t\t [2] Chuveiros ");
		printf("\n\t\t [3] Vestiários ");
		printf("\n\t\t [4] Armários ");
		printf("\n\t\t [5] Locais para refeição ");
		printf("\n\t\t [6] Alojamento ");
		printf("\n\t\t [7] Sair ");
		printf("\n\t\t Escolha: ");
			scanf("%d", &op);
			
			while (op <= 0  || op >= 8)
					{
						printf("\n\t\t Opção inválida!");
						printf("\n\t\t Digite uma opção válida.");
						printf("\n\t\t Escolha:  ");
							scanf("\t %d", &op);	
					}
						
							switch (op)
							{
								case 1:
									printf("\n\n\t NR 24, item 24.2 Instalações sanitárias");
									printf("\n\n\t Instalações separadas por sexo.");
									printf("\n\n\t Instalações sanitárias masculinas: Estabelecimento construídos ");
									printf("\n\t até 23/09/2019: Vide Portaria MTb nº 3214/1978.");
					
									printf("\n\n\t A partir de 24/09/2019: uma unidade para cada 20 trabalhadores, ");
									printf("\n\t até 100 trabalhadores. E uma unidade para cada 50, no que exceder.");
										
									
									printf("\n\n\t Será exigido um lavatório para cada 10 trabalhadores nas atividades");
									printf("\n\t com exposição e manuseio de materal infectante.");
										
									printf("\n\n\t Funções comerciais, administrativas e similares: até 10 trabalhadores,");
									printf("\n\t 1 instalação sanitária; podendo ser de uso comum, desde que respeite ");
									printf("\n\t as condições de privacidades. ");
									
									
								break;
								case 2:
									printf("\n\n\t NR 24, item 24.3 Chuveiros");
									printf("\n\n\t Se houver exigência de chuveiros, estes devem fazer parte ou");
									printf("\n\t estar anexos aos vestiários.");
									printf("\n\n\t Será exigido 1 chuveiro para cada grupo de: ");
									printf("\n\t 10 trabalhadores com exposição e manuseio de material infectante.");
									printf("\n\t 20 trabalhadores para atividades com poeiras, esforço físico ou ");
									printf("\n\t ou submetidos a condições ambientais de calor intenso.");
									
								break;
								case 3:
									printf("\n\n\t NR 24, item 24.4 Vestiários");
									printf("\n\n\t24.4.1 Todos os estabelecimentos devem ser dotados de vestiários quando: ");
									printf("\n\t\ta) a atividade exija a utilização de vestimentas de trabalho ou que seja imposto o uso de uniforme ");
									printf("\n\t\tcuja troca deva ser feita no próprio local de trabalho; ou ");
									printf("\n\t\tb) a atividade exija que o estabelecimento disponibilize chuveiro. ");
								
									printf("\n\n\t24.4.2 Os vestiários devem ser dimensionados em função do número de trabalhadores ");
									printf("\n\tque necessitam utilizá-los, até o limite de 750 (setecentos e cinquenta) trabalhadores, conforme o ");
									printf("\n\tseguinte cálculo: área mínima do vestiário por trabalhador = 1,5 - (nº de trabalhadores / 1000). ");
								
									printf("\n\n\t24.4.2.1 Em estabelecimentos com mais de 750 (setecentos e cinquenta) trabalhadores, ");
									printf("\n\tos vestiários devem ser dimensionados com área de, no mínimo, 0,75m² (setenta e cinco decímetros quadrados)");
									printf("\n\tpor trabalhador.");
									printf("\n\n\tQual a quantidade de trabalhadores? ");
										scanf("%f", &trabalhadores);
										while (trabalhadores > 750)
											{
												printf("\n\t Opção inválida! Lembre-se do limite de até 750 colaboradores. ");
												printf("\n\t Digite novamente ");
												printf("\n\n\t Digite a quantidade de trabalhadores nessa posição (Limite de 750): ");
													scanf("\t%f", &trabalhadores);
											}
											areaMin = 1.5 - trabalhadores / 1000 ;
											
											printf("\n\tÁrea mínima do vestiário por trabalhador (Limite de 750):  %.2f m²", areaMin);	
												
												
												
								break;
								case 4:
									printf("\n\n\t NR 24, item 24.4.4 Armários");
									printf("\n\n\t24.4.4 É admitido o uso rotativo de armários simples entre usuários, exceto nos casos em que ");
									printf("\n\testes sejam utilizados para a guarda de Equipamentos de Proteção Individual - EPI e de vestimentas ");
									printf("\n\texpostas a material infectante, substâncias tóxicas, irritantes ou que provoquem sujidade. ");
									
									printf("\n\n\t24.4.5 Nas atividades laborais em que haja exposição e manuseio de material infectante, substâncias"); 
									printf("\n\ttóxicas, irritantes ou aerodispersóides, bem como naquelas em que haja contato com substâncias que ");
									printf("\n\tprovoquem deposição de poeiras que impregnem a pele e as roupas do trabalhador devem ser fornecidos ");
									printf("\n\tarmários de compartimentos duplos ou dois armários simples. ");
									
									printf("\n\n\t24.4.5.1 Ficam dispensadas de disponibilizar 2 (dois) armários simples ou armário duplo as organizações");
									printf("\n\tque promovam a higienização diária de vestimentas ou que forneçam vestimentas descartáveis, ");
									printf("\n\tassegurada a disponibilização de 1 (um) armário simples para guarda de roupas comuns de uso pessoal ");
									printf("\n\tdo trabalhador.");
									
									printf("\n\n\t24.4.7 As empresas que oferecerem serviços de guarda volume para a guarda de roupas e acessórios ");
									printf("\n\tpessoais dos trabalhadores estão dispensadas de fornecer armários.");
									
									printf("\n\n\t24.4.8 Nas empresas desobrigadas de manter vestiário, deve ser garantido o fornecimento de escaninho,"); 
									printf("\n\tgaveta com tranca ou similar que permita a guarda individual de pertences pessoais dos trabalhadores ou ");
									printf("\n\tserviço de guarda-volumes.");


								break;
								case 5:
									printf("\n\n\t NR 24, item 24.5 Locais para refeição");
									
									printf("\n\n\t24.5.2 Os locais para tomada de refeições para atender até 30 (trinta) trabalhadores, observado o subitem 24.5.1.1, devem: ");
									printf("\n\t\ta) ser destinados ou adaptados a este fim; ");
									printf("\n\t\tb) ser arejados e apresentar boas condições de conservação, limpeza e higiene; e ");
									printf("\n\t\tc) possuir assentos e mesas, balcões ou similares suficientes para todos os usuários atendidos. ");
								
									printf("\n\n\t24.5.2.1 A empresa deve garantir, nas proximidades do local para refeições: ");
									printf("\n\t\ta) meios para conservação e aquecimento das refeições; ");
									printf("\n\t\tb) local e material para lavagem de utensílios usados na refeição; e ");
									printf("\n\t\tc) água potável. ");
								
									printf("\n\n\t24.5.3 Os locais destinados às refeições para atender mais de 30 (trinta) trabalhadores, conforme subitem 24.5.1.1, devem: ");
									printf("\n\t\ta) ser destinados a este fim e fora da área de trabalho; ");
									printf("\n\t\tb) ter pisos revestidos de material lavável e impermeável; ");
									printf("\n\t\tc) ter paredes pintadas ou revestidas com material lavável e impermeável; ");
									printf("\n\t\td) possuir espaços para circulação; ");
									printf("\n\t\te) ser ventilados para o exterior ou com sistema de exaustão forçada, salvo em ambientes climatizados artificialmente; ");
									printf("\n\t\tf) possuir lavatórios instalados nas proximidades ou no próprio local, atendendo aos requisitos do subitem 24.3.4; ");
									printf("\n\t\tg) possuir assentos e mesas com superfícies ou coberturas laváveis ou descartáveis, em número correspondente aos usuários atendidos;"); 
									printf("\n\t\th) ter água potável disponível; ");
									printf("\n\t\ti) possuir condições de conservação, limpeza e higiene; ");
									printf("\n\t\tj) dispor de meios para aquecimento das refeições; e ");
									printf("\n\t\tk) possuir recipientes com tampa para descarte de restos alimentares e descartáveis. ");
									
									printf("\n\n\t24.5.4 Ficam dispensados das exigências do item 24.5 desta NR: ");
									printf("\n\t\ta) estabelecimentos comerciais bancários e atividades afins que interromperem suas atividades por 2 (duas) horas, no período ");
									printf("\n\t\tdestinado às refeições; ");
									printf("\n\t\tb) estabelecimentos industriais localizados em cidades do interior, quando a empresa mantiver vila operária ou residirem, seus"); 
									printf("\n\t\ttrabalhadores, nas proximidades, permitindo refeições nas próprias residências. ");
									printf("\n\t\tc) os estabelecimentos que oferecerem vale-refeição, desde que seja disponibilizado condições para conservação e aquecimento da ");
									printf("\n\t\tcomida, bem como local para a tomada das refeições pelos trabalhadores que trazem refeição de casa. ");

									
									
								break;
								case 6:
									printf("\n\n\t NR 24, item 24.7 Alojamento");
									printf("\n\n\t24.7.1 Alojamento é o conjunto de espaços ou edificações, composto de dormitório, ");
									printf("\n\tinstalações sanitárias, refeitório, áreas de vivência e local para lavagem e secagem de roupas, ");
									printf("\n\tsob responsabilidade do empregador, para hospedagem temporária de trabalhadores. ");
									
									printf("\n\n\t24.7.2 Os dormitórios dos alojamentos devem: ");
									printf("\n\t\ta) ser mantidos em condições de conservação, higiene e limpeza; ");
									printf("\n\t\tb) ser dotados de quartos; ");
									printf("\n\t\tc) dispor de instalações sanitárias, respeitada a proporção de 01 (uma) instalação ");
									printf("\n\t\tsanitária com chuveiro para cada 10 (dez) trabalhadores hospedados ou fração; e ");
									printf("\n\t\td) ser separados por sexo. ");
									
									printf("\n\n\t24.7.2.1. Caso as instalações sanitárias não sejam parte integrante dos dormitórios, ");
									printf("\n\tdevem estar localizadas a uma distância máxima de 50 m (cinquenta metros) dos mesmos, ");
									printf("\n\tinterligadas por passagens com piso lavável e cobertura. ");
									
									printf("\n\n\t24.7.3 Os quartos dos dormitórios devem: ");
									printf("\n\t\ta) possuir camas correspondente ao número de trabalhadores alojados no quarto, vedado ");
									printf("\n\t\to uso de 3 (três) ou mais camas na mesma vertical, e ter espaçamentos vertical e horizontal ");
									printf("\n\t\tque permitam ao trabalhador movimentação com segurança; ");
									printf("\n\t\tb) possuir colchões certificados pelo INMETRO; ");
									printf("\n\t\tc) possuir colchões, lençóis, fronhas, cobertores e travesseiros limpos e higienizados, ");
									printf("\n\t\tadequados às condições climáticas; ");
									printf("\n\t\td) possuir ventilação natural, devendo esta ser utilizada conjuntamente com a ventilação ");
									printf("\n\t\tartificial, levando em consideração as condições climáticas locais; ");
									printf("\n\t\te) possuir capacidade máxima para 8 (oito) trabalhadores; ");
									printf("\n\t\tf) possuir armários; ");
									printf("\n\t\tg) ter, no mínimo, a relação de 3,00 m² (três metros quadrados) por cama simples ou ");
									printf("\n\t\t4,50 m² (quatro metros e cinquenta centímetros quadrados) por beliche, em ambos os casos"); 
									printf("\n\t\tincluídas a área de circulação e armário; e ");
									printf("\n\t\th) possuir conforto acústico conforme NR17. ");
										
									printf("\n\n\t24.7.3.1 As camas superiores dos beliches devem ter proteção lateral e escada fixas à");
									printf("\n\testrutura. ");
										
									printf("\n\n\t24.7.3.2 Os armários dos quartos devem ser dotados de sistema de trancamento e com ");
									printf("\n\tdimensões compatíveis para a guarda de roupas e pertences pessoais do trabalhador, e enxoval ");
									printf("\n\tde cama.");
									
									printf("\n\n\t24.7.4 Os trabalhadores alojados no mesmo quarto devem pertencer, preferencialmente, ");
									printf("\n\tao mesmo turno de trabalho.");
									
									printf("\n\n\t24.7.5 Os locais para refeições devem ser compatíveis com os requisitos do item 24.5");
									printf("\n\tdesta NR, podendo ser parte integrante do alojamento ou estar localizados em ambientes externos. ");
								
									printf("\n\n\t24.7.5.1 Quando os locais para refeições não fizerem parte do alojamento, deverá ser ");
									printf("\n\tgarantido o transporte dos trabalhadores.");
									
									printf("\n\n\t24.7.6 Os alojamentos devem dispor de locais e infraestrutura para lavagem e secagem ");
									printf("\n\tde roupas pessoais dos alojados ou ser fornecido serviço de lavanderia.");
								
									printf("\n\n\t24.7.8 Deve ser garantida coleta de lixo diária, lavagem de roupa de cama, manutenção ");
									printf("\n\tdas instalações e renovação de vestuário de camas e colchões.");

								break;
								case 7:
									printf("\n\n\t Até a próxima! \n\n");
									system ("pause");
									return 0;
								break;
							}
						
		printf("\n\n\t Deseja realizar outra consulta? ");
		printf("\n\t [1] Sim \n\t [2] Não")	;
		printf("\n\t Escolha:  ");
			scanf("\t %d", &retorno );
			while (retorno <1 || retorno >2 )
				{
						printf("\n\t Opção inválida! ");
						printf("\n\t Digite novamente ");
						printf("\n\n\t [1] Sim \n\t [2] Não");
						printf("\n\t Escolha: \t");
						scanf("\t %d", &retorno );
				}
					if (retorno == 1)
					{
						system("cls");
						return main ();
					}
					else printf("\n\n\tObrigado! Até mais...\n");
				

}

float insalubridade ()
{
	int retorno, op, baseSalarial;
	float pisoSalarial, insalubre;
	
	printf("\n\n\t Qual o grau de insalubridade?   ");
	printf("\n\n\t [1] Grau mínimo (10%%) \n\t [2] Grau médio (20%%) \n\t [3] Grau máximo (40%%) ");
	printf("\n\t Escolha:  ");
		scanf("\t %d", &op);	
		while (op <= 0  || op >= 4)
			{
				printf("\n\t\t Opção inválida!");
				printf("\n\t\t Digite uma opção válida.");
				printf("\n\t\t Escolha:  ");
					scanf("\t %d", &op);	
			}
			
			switch (op)
			{
				case 1:
					printf("\n\n\t Qual base salarial será usada?");
					printf("\n\n\t [1] Piso-salarial \n\t [2] Salário mínimo \n\t [3] Convenção social");
					printf("\n\t Escolha: ");
						scanf("\t %d", &baseSalarial);
						while (baseSalarial <= 0  || baseSalarial >= 4)
							{
								printf("\n\t\t Opção inválida!");
								printf("\n\t\t Digite uma opção válida.");
								printf("\n\t\t Escolha:  ");
									scanf("\t %d", &baseSalarial);	
							}
							if (baseSalarial == 1)
								{
									printf("\n\n\t Qual o valor do piso-salarial para cálculo? ");	
									printf("\n\t Piso-salarial: R$ ");
										scanf("\t %f", &pisoSalarial);
									insalubre = pisoSalarial * 1.1;
									printf("\n\t Salário com reajuste de 10%% referente a insalubridade grau mínimo: R$ %.2f", insalubre); 	
								}
								else if (baseSalarial == 2)
									{
										printf("\n\n\t A última atualização de salário mínimo encontrada é de R$ 1.045,00 ");	
								
										
										insalubre = 1045 * 1.1;
										printf("\n\t Salário com reajuste de 10%% referente a insalubridade grau mínimo: R$ %.2f", insalubre); 
									}
									else if (baseSalarial == 3)
											{
												printf("\n\n\t Qual o valor acordado na convenção para cálculo? ");	
												printf("\n\t Convenção social: R$ ");
													scanf("\t %f", &pisoSalarial);	
												insalubre = pisoSalarial * 1.1;
												printf("\n\t Salário com reajuste de 10%% referente a insalubridade grau mínimo: R$ %.2f", insalubre); 
											}
				break;	
				case 2:
					printf("\n\n\t Qual base salarial será usada?");
						printf("\n\n\t [1] Piso-salarial \n\t [2] Salário mínimo \n\t [3] Convenção social");
						printf("\n\t Escolha: ");
							scanf("\t %d", &baseSalarial);
							while (baseSalarial <= 0  || baseSalarial >= 4)
								{
									printf("\n\t\t Opção inválida!");
									printf("\n\t\t Digite uma opção válida.");
									printf("\n\t\t Escolha:  ");
										scanf("\t %d", &baseSalarial);	
								}
								if (baseSalarial == 1)
									{
										printf("\n\n\t Qual o valor do piso-salarial para cálculo? ");	
										printf("\n\t Piso-salarial: R$ ");
											scanf("\t %f", &pisoSalarial);
										insalubre = pisoSalarial * 1.2;
										printf("\n\t Salário com reajuste de 20%% referente a insalubridade grau médio: R$ %.2f", insalubre); 	
									}
									else if (baseSalarial == 2)
										{
											printf("\n\n\t A última atualização de salário mínimo encontrada é de R$ 1.045,00 ");	
									
											
											insalubre = 1045 * 1.2;
											printf("\n\t Salário com reajuste de 20%% referente a insalubridade grau médio: R$ %.2f", insalubre); 
										}
										else if (baseSalarial == 3)
												{
													printf("\n\n\t Qual o valor acordado na convenção para cálculo? ");	
													printf("\n\t Convenção social: R$ ");
														scanf("\t %f", &pisoSalarial);	
													insalubre = pisoSalarial * 1.2;
													printf("\n\t Salário com reajuste de 20%% referente a insalubridade grau médio: R$ %.2f", insalubre); 
												}
				
				
				break;
				case 3:
					printf("\n\n\t Qual base salarial será usada?");
						printf("\n\n\t [1] Piso-salarial \n\t [2] Salário mínimo \n\t [3] Convenção social");
						printf("\n\t Escolha: ");
							scanf("\t %d", &baseSalarial);
							while (baseSalarial <= 0  || baseSalarial >= 4)
								{
									printf("\n\t\t Opção inválida!");
									printf("\n\t\t Digite uma opção válida.");
									printf("\n\t\t Escolha:  ");
										scanf("\t %d", &baseSalarial);	
								}
								if (baseSalarial == 1)
									{
										printf("\n\n\t Qual o valor do piso-salarial para cálculo? ");	
										printf("\n\t Piso-salarial: R$ ");
											scanf("\t %f", &pisoSalarial);
										insalubre = pisoSalarial * 1.4;
										printf("\n\t Salário com reajuste de 40%% referente a insalubridade grau máximo: R$ %.2f", insalubre); 	
									}
									else if (baseSalarial == 2)
										{
											printf("\n\n\t A última atualização de salário mínimo encontrada é de R$ 1.045,00 ");	
									
											
											insalubre = 1045 * 1.4;
											printf("\n\t Salário com reajuste de 40%% referente a insalubridade grau máximo: R$ %.2f", insalubre); 
										}
										else if (baseSalarial == 3)
												{
													printf("\n\n\t Qual o valor acordado na convenção para cálculo? ");	
													printf("\n\t Convenção social: R$ ");
														scanf("\t %f", &pisoSalarial);	
													insalubre = pisoSalarial * 1.4;
													printf("\n\t Salário com reajuste de 40%% referente a insalubridade grau máximo: R$ %.2f", insalubre); 
												}
				
				break;
			}
	
	
	printf("\n\n\t Deseja realizar outra consulta? ");
	printf("\n\t [1] Sim \n\t [2] Não")	;
	printf("\n\t Escolha:  ");
		scanf("\t %d", &retorno );
		while (retorno <1 || retorno >2 )
			{
					printf("\n\t Opção inválida! ");
					printf("\n\t Digite novamente ");
					printf("\n\n\t [1] Sim \n\t [2] Não");
					printf("\n\t Escolha: \t");
					scanf("\t %d", &retorno );
			}
				if (retorno == 1)
				{
					system("cls");
					return main ();
				}
				else printf("\n\n\tObrigado! Até mais...\n");
	
}

float periculosidade ()
{
	float salario, periculosidade;
	int retorno;
	
	printf("\n\n\t Qual o salário base do trabalhador?  R$ ");
		scanf("%f", &salario);
	periculosidade = salario * 1.3;
	printf("\n\t O salário com reajuste de 30%% referente ao adicional de periculosidade será de:  R$ %.2f", periculosidade);
	
	printf("\n\n\t Deseja realizar outra consulta? ");
	printf("\n\t [1] Sim \n\t [2] Não")	;
	printf("\n\t Escolha:  ");
		scanf("\t %d", &retorno );
		while (retorno <1 || retorno >2 )
			{
					printf("\n\t Opção inválida! ");
					printf("\n\t Digite novamente ");
					printf("\n\n\t [1] Sim \n\t [2] Não");
					printf("\n\t Escolha: \t");
					scanf("\t %d", &retorno );
			}
				if (retorno == 1)
				{
					system("cls");
					return main ();
				}
				else printf("\n\n\tObrigado! Até mais...\n");
	
	
}

float pintura ()
{
		int retorno, i, demaos,porta,janela, qtdporta = 0, qtdjanela = 0;
	float largura,altura,area,plargura,paltura,parea,jlargura,jaltura,jarea,rendimento,areatotal,qtd,qtdtotal;
	
	printf ("\n---------------------------- Informação Muito Importante ------------------------------");
	printf ("\nProcure Sempre Fabricantes Confiáveis, para fins de Cálculos usamos como base os 3 fabricantes mais famosos do mundo. \n1 - Sherwin-Williams. \n2 - Suvinil. \n3 - Coral.\nObs: Outras marcas de Tintas podem ser consideradas porém os cálculos podem sofrer uma leve alteração na quantidade devido a sua composição.");
	
	printf ("\n\n--------- Dimensionamento da Parede em M ------------");
	printf ("\n\nInforme a Largura da parede que deseja pintar em M..:");
	scanf ("%f", &largura);
	printf ("Informe a Altura da parede que deseja pintar M..:");
	scanf ("%f", &altura);
	area = largura*altura;
	printf ("Area da Parede..:%.2fM²", area);
	//area da parede
	
	printf ("\n\nDigite Se Possui Porta de acordo com o Determinado..: \n 1 - Sim \n 2 - Não");
	printf ("\n\nPossui Porta ?..:");
	scanf ("%d", &porta);
	if (porta != 1 );
	// verificando valor verdade
	{ 
	printf ("\n----------- Dimensionamento da Porta Será excluído o espaço no Cálculo ------------");
	printf ("\n\nInforme a Largura da Porta que encontra-se na parede que deseja pintar em M..:");
	scanf ("%f", &plargura);
	printf ("Informe a Altura da Porta que encontra-se na parede que deseja pintar em M..:");
	scanf ("%f", &paltura);
	parea = paltura*plargura;
	printf ("Area da Porta..:%.2fM²", parea);
	}
	
	printf ("\n\nDigite se Possui Janela de acordo com o Determinado..: \n 1 - Sim \n 2 - Não");
	printf ("\n\nPossui Janela ?..:");
	scanf ("%d", &janela);
	
	// verificando valor verdade
	if (janela != 1 )
	{
	printf ("\n---------- Dimensionamento da Janela Será excluído o espaço no Cálculo ------------");
	printf ("\n\nInforme a Largura da janela que encontra-se na parede que deseja pintar em M..:");
	scanf ("%f", &jlargura);
	printf ("Informe a Altura da janela que econtra-se na parede que deseja pintar em M..:");
	scanf ("%f", &jaltura);
	jarea = jaltura*jlargura;
	printf ("Area da Janela..:%.2fM²", jarea);	
	}
	// informações adicionais
	printf ("\n\nInforme a Quantidade de demãos..:");
	scanf ("%d", &demaos);
	printf ("\nRendimento do Fabricante..:(recomendado 10M² por Litro)..:? ");
	scanf ("%f", &rendimento);	
	
	
	// calculo
	areatotal = area - parea - jarea;
	qtd = areatotal * demaos;
	qtdtotal = qtd/rendimento;
	 

	printf ("\nArea Total a Ser Pintada..:%.2fM²", areatotal);
	printf ("\nTotal de Tinta Necessário para Pintura..:%.2f Litros", qtdtotal);	

	printf("\n\n\t Deseja realizar outra consulta? ");
	printf("\n\t [1] Sim \n\t [2] Não")	;
	printf("\n\t Escolha:  ");
		scanf("\t %d", &retorno );
		while (retorno <1 || retorno >2 )
			{
					printf("\n\t Opção inválida! ");
					printf("\n\t Digite novamente ");
					printf("\n\n\t [1] Sim \n\t [2] Não");
					printf("\n\t Escolha: \t");
					scanf("\t %d", &retorno );
			}
				if (retorno == 1)
				{
					system("cls");
					return main ();
				}
				else printf("\n\n\tObrigado! Até mais...\n");
	
}

float arcondicionado ()
{
	float area;
	int retorno;
	
	printf ("Digite a area(m²)..:");
 		scanf ("%f",&area);
  
  if(area<=9)
	  	{
		  printf("Ar condicionado de 7000 BTUs para um ambiente residencial.\n");
		  printf("Ar condicionado de 7000 BTUs para um ambiente comercial.");
		}
	  
	  	else if(area>9 && area<=12)
		  {
			  printf ("Ar condicionado de 7000 BTUs para um ambiente residencial.\n");
			  printf("Ar condicionado de 9000 BTUs para um ambiente comercial.");
		  }
		  
		  else if(area>12 && area<=15)
			  {
				  printf("Ar condicionado de 9000 BTUs para um ambiente residencial.\n");
				  printf("Ar condicionado de 12000 BTUs para um ambiente comercial");
			  }
			  
			  else if(area>15 && area<=20)
				  {
					  printf("Ar condicionado de 12000 BTUs para um ambiente residencial.\n");
					  printf("Ar condicionado de 16000 BTUs para um ambiente comercial.");
				  }
				  
				  else if(area>20 && area<=25)
					  {
						  printf("Ar condicionado de 15000 BTUs para um ambiente residencial\n");
						  printf("Ar condicionado de 20000 BTUs para um ambiente comercial.");
					  }
					  
					  else if(area>25 && area<=30)
						  {
							  printf("Ar condicionado de 18000 BTUs para um ambiente residencial.\n");
							  printf("Ar condicionado de 24000 BTUs para um ambiente comercial.");
						  }
						  
						  else if(area>30 && area<=35)
							  {
								  printf("Ar condicionado de 21000 BTUs para um ambiente residencial.\n");
								  printf("Ar condicionado de 28000 BTUs para um ambiente comercial.");
							  }
							  
							  else if(area>35 && area<=40)
								  {
									  printf("Ar condicionado de 24000 BTUs para um ambiente residencial.\n");
									  printf("Ar condicionado de 32000 BTUs para um ambiente comercial.");
								  }
								  
								  else if(area>40 && area<=45)
									  {
										  printf("Ar condicionado de 27000 BTUs para um ambiente residencial.\n");
										  printf("Ar condicionado de 36000 BTUs para um ambiente comercial.");
									  }
									  
									  else if(area>45 && area<=50)
										  {
											  printf("Ar condicionado de 30000 BTUs para um ambiente residencial.\n");
											  printf("Ar condicionado de 40000 BTUs para um ambiente comercial.");
										  }
										  
										  else if(area>50 && area<=60)
											  {
												  printf("Ar condicionado de 36000 BTUs para um ambiente residencial.\n");
												  printf("Ar condicionado de 48000 BTUs para um ambiente comercial.");
											  }
											  
											  else if(area>60 && area<=70)
												  {
													  printf("Ar condicionado de 42000 BTUs para um ambiente residencial.\n");
													  printf("Ar condicionado de 56000 BTUs para um ambiente comercial.");
												  }
												  
	printf("\n\n\t Deseja realizar outra consulta? ");
	printf("\n\t [1] Sim \n\t [2] Não")	;
	printf("\n\t Escolha:  ");
		scanf("\t %d", &retorno );
		while (retorno <1 || retorno >2 )
			{
					printf("\n\t Opção inválida! ");
					printf("\n\t Digite novamente ");
					printf("\n\n\t [1] Sim \n\t [2] Não");
					printf("\n\t Escolha: \t");
					scanf("\t %d", &retorno );
			}
				if (retorno == 1)
				{
					system("cls");
					return main ();
				}
				else printf("\n\n\tObrigado! Até mais...\n");
	
}

float tijolo ()
{
	int retorno, op;

    printf("\nMenu de opções \n\n");
    printf("Digite qual tijolo será:\t");
    printf("\n digite [1] para tijolo de 6 furos \t");
    printf("\n digite [2] para tijolo de 8 furos \t");
    printf("\n digite [3] para tijolo de 9 furos \t");
    printf("\n\n Escolha a opção desejada:");
    scanf("%d", &op);
    
    switch (op)
    {
        case 1:
        seisFuros();
        break;
        
        case 2: 
        oitoFuros();
        break;
        
        case 3: 
        noveFuros();
        break;
        
        
        printf("\n\tOpção Inválida");
    };
 
}

float seisFuros()
{
	    float tijlo1=0.0266, altura1, largura1, compri1;
	    float totalTijolo1;
	    int retorno;
	    
    printf("\n\t Ao digitar, use vírgula (,) para separar as casas decimais.");
	    printf("\n\n Digite a altura do comodo:  ");
	    scanf("%f", &altura1);
	    printf("\n Digite a largura do comodo:  ");
	    scanf("%f", &largura1);
	    printf("\n Digite o comprimento do comodo:  ");
	    scanf("%f", &compri1);
	    
	    totalTijolo1 = altura1 * largura1 * compri1 / tijlo1;
	    printf("\n Total de tijolo: %f", totalTijolo1);
		printf("\n\n\t Muito obrigado pela participação!");
			
			
			printf("\n\n\t Deseja realizar outra consulta? ");
			printf("\n\t [1] Sim \n\t [2] Não")	;
			printf("\n\t Escolha:  ");
				scanf("\t %d", &retorno );
				while (retorno <1 || retorno >2 )
					{
							printf("\n\t Opção inválida! ");
							printf("\n\t Digite novamente ");
							printf("\n\n\t [1] Sim \n\t [2] Não");
							printf("\n\t Escolha: \t");
							scanf("\t %d", &retorno );
					}
						if (retorno == 1)
						{
							system("cls");
							return main ();
						}
						else printf("\n\n\tObrigado! Até mais...\n");
	    
}
	
float oitoFuros()
{
	    float tijlo2=0.0361, altura2, largura2, compri2;
	 	float totalTijolo2;
	 	int retorno;
	 	
    printf("\n\t Ao digitar, use vírgula (,) para separar as casas decimais.");
	    printf("\n\n Digite a altura do comodo:  ");
	    scanf("%f", &altura2);
	    printf("\n Digite a largura do comodo:  ");
	    scanf("%f", &largura2);
	    printf("\n Digite o comprimento do comodo:  ");
	    scanf("%f", &compri2);
	
	    
	    totalTijolo2 = altura2 * largura2 * compri2 / tijlo2;
	    printf("\n Total de tijolo: %f", totalTijolo2);
	    printf("\n\n\t Muito obrigado pela participação!");  
		 
	    	printf("\n\n\t Deseja realizar outra consulta? ");
			printf("\n\t [1] Sim \n\t [2] Não")	;
			printf("\n\t Escolha:  ");
				scanf("\t %d", &retorno );
				while (retorno <1 || retorno >2 )
					{
							printf("\n\t Opção inválida! ");
							printf("\n\t Digite novamente ");
							printf("\n\n\t [1] Sim \n\t [2] Não");
							printf("\n\t Escolha: \t");
							scanf("\t %d", &retorno );
					}
						if (retorno == 1)
						{
							system("cls");
							return main ();
						}
						else printf("\n\n\tObrigado! Até mais...\n");
	}
	
float noveFuros()
{
	   float tijlo3=0.0366, altura3, largura3, compri3;
	   float totalTijolo3;
	   int retorno; 
	    
    printf("\n\t Ao digitar, use vírgula (,) para separar as casas decimais.");
	    printf("\n\n Digite a altura do comodo:  ");
	    scanf("%f", &altura3);
	    printf("\n Digite a largura do comodo:  ");
	    scanf("%f", &largura3);
	    printf("\n Digite o comprimento do comodo:  ");
	    scanf("%f", &compri3);
	    
	    totalTijolo3 = altura3 * largura3 * compri3 / tijlo3;
	    printf("\n Total de tijolo: %f", totalTijolo3);
	    printf("\n\n\t Muito obrigado pela participação!");  
	    
	    	printf("\n\n\t Deseja realizar outra consulta? ");
			printf("\n\t [1] Sim \n\t [2] Não")	;
			printf("\n\t Escolha:  ");
				scanf("\t %d", &retorno );
				while (retorno <1 || retorno >2 )
					{
							printf("\n\t Opção inválida! ");
							printf("\n\t Digite novamente ");
							printf("\n\n\t [1] Sim \n\t [2] Não");
							printf("\n\t Escolha: \t");
							scanf("\t %d", &retorno );
					}
						if (retorno == 1)
						{
							system("cls");
							return main ();
						}
						else printf("\n\n\tObrigado! Até mais...\n");
	
}

float piso ()
{
	// VARIAVEIS
float metrcomodo,mmlargura,mmespessura,metrpiso,mmcomp,argamassa,consumorejunte,consumorejunte2,consumorejunte3,mmlarg;
int retorno, calculo,adicional,largrejunte, resposta, tipor;
//ENTRADA DE DADOS

do
	{

		printf("------------Nos informe os seguintes dados------------");
		printf("\nDigite o metro quadrado do comodo onde deseja colocar o piso..: ");
			scanf("%f", &metrcomodo);
		printf("Digite a largura em milímetros da unidade de piso que deseja colocar em seu cômodo..:");
			scanf("%f",&mmlargura);
		printf("Digite o comprimento em milímetros da unidade de piso que deseja colocar em seu cômodo..:");
			scanf("%f", &mmcomp);
		 printf("Digite a espessura em milímetros da unidade de piso que deseja colocar em seu cômodo..:");
			 scanf("%f",&mmespessura);
		 printf("Digite o milímetros da largura do rejunte mínimo recomendada pelo fabricante (essa informação deverá estar na caixa)..:");
			 scanf("%f", &mmlarg);
		 printf("Digite o número do rejunte que você irá utilizar..:\n1-Epóxi\n2-Acrílico\n3-Rejunte sobre rejunte\n");
			 scanf("%i", &tipor);
		
		
		// PROCESSAMENTO E SAIDA DE DADOS
		
		//calculo argamassa
		argamassa = 5 * metrcomodo;
		printf("\n\nA quantidade necessária de argamassa colante para assentar é de...:%.2f kg", argamassa);
		//calculo quantidade de pisos
		metrpiso = (mmlargura/1000) *(mmcomp/1000);
		calculo = metrcomodo/metrpiso;
		printf("\nA quantidade de pisos que deve comprar é de..:%i unidades", calculo);
		//calculo adicional recomendado
		adicional = calculo * 1.10;
		printf("\nPara evitar imprevistos,como acidentes com o material, aconselhamos comprar um adicional de 10%%, totalizando..:%i unidades", adicional);
		//calculo consumo de rejunte
		//epoxi
		    if (tipor==1){
		
		    consumorejunte =metrcomodo * ((mmlargura+mmcomp) * mmespessura * mmlarg * 1.58)/(mmlargura*mmcomp);
		    printf("\nCaso use o rejunte Epóxi,o consumo será de..:%.2f Kg", consumorejunte);
		}
		//acrilico
		else if(tipor==2){
		
		    consumorejunte2 = metrcomodo * ((mmlargura+mmcomp) * mmespessura * mmlarg * 1.75)/(mmlargura*mmcomp);
		    printf("\nCaso use o rejunte Acrílico,o consumo será de..:%.2f Kg", consumorejunte2);
		}
		//rejunte sobre rejunte    
		    else if (tipor==3){
		
		    consumorejunte3 = metrcomodo * ((mmlargura+mmcomp) * mmespessura * mmlarg * 1.32)/(mmlargura*mmcomp);
		    printf("\nCaso use o rejunte sobre rejunte,o consumo será de..:%.2f Kg", consumorejunte3);
		}
		// PERGUNTA PARA A REPETIÇÃO
		printf("\n\n\n\nDigite o numero correspondente ao que deseja fazer..:\n1-Adicionar mais um projeto\n2-Finalizar");
			scanf("%i",&resposta);
	}while (resposta==1);
	
	printf("\n\n\t Deseja realizar outra consulta? ");
			printf("\n\t [1] Sim \n\t [2] Não")	;
			printf("\n\t Escolha:  ");
				scanf("\t %d", &retorno );
				while (retorno <1 || retorno >2 )
					{
							printf("\n\t Opção inválida! ");
							printf("\n\t Digite novamente ");
							printf("\n\n\t [1] Sim \n\t [2] Não");
							printf("\n\t Escolha: \t");
							scanf("\t %d", &retorno );
					}
						if (retorno == 1)
						{
							system("cls");
							return main ();
						}
						else printf("\n\n\tObrigado! Até mais...\n");
}

float venda ()
{
	
int qtdSP, continuar, op, codigo, compras, qtdSuvinil, qtdCoral, qtdKit;
	char nome[30], cpf[11], nascimento[8], rua[40], numero[5], bairro[20], estado[20];
	float total;

		printf("\n------------LOJA ONLINE [GREEN BUILDING], SUA CONSTRUÇÃO VERDE!-----------");
		printf("\n\n--------------------------CATÁLOGO GREEN BUILDING-------------------------");
		printf("\n\n\tCódigo \t\t\t\t Preço\t\t\t");
		printf("\n\t1 Tinta Suvinil Azul 3,6L \t R$ 73,00 \t\t ");
		printf("\n\t2 Tinta Coral Branco 3,6L \t R$ 79,00 \t\t ");
		printf("\n\t3 Tinta Coral Preto 3,6L \t R$ 74,90 \t\t ");
		printf("\n\n--------------------------------------------------------------------------");
		printf("\n--------------------------------------------------------------------------");
		printf("\n\n--------------------------------------------------------------------------");
		printf("\n\t Olá! Vamos iniciar a sua venda. \n\t Digite o código do produto: " );
		scanf("%d", &codigo);
					while (codigo < 0 || codigo > 3)
										{
											printf("\n\t\tPoxa, não temos esse produto! \n\t\t Digite outro código: ");
												scanf("%d", &codigo);
										}
					if (codigo==1)
						{
							
								printf("\n\t\tTinta Suvinil Azul 3,6L \n\t\t Digite a quantidade desejada: ");
									scanf("%d", &qtdSuvinil);
								printf("\n\tQuantidade escolhida: %d", qtdSuvinil);
								fflush(stdin);
								printf("\n\t Próximo passo: \n\t\t [1] Excluir produto \n\t\t [2] Continuar");
								printf("\n\t\tEscolha: ");
									scanf("%d", &continuar);
									if (continuar ==1)
									{
										printf("\n\t Ok, estou excluindo seus produtos do carrinho...");
										printf("\n\n\t Vou abrir o catálogo para você escolher novamente. \n\n");
										venda ();		
									}
									
									else if (continuar ==2)
										{
											fflush(stdin);
											printf("\n\n\t Agora vamos agilizar as coisas para a sua entrega! ");
											printf("\n\tInforme \n\t\t - Nome: ");
												gets(nome); strupr(nome); fflush(stdin);
											printf("\n\t\t - CPF(Somente números): "); 
												gets(cpf); fflush(stdin);
											printf("\n\t\t - Data de nascimento (11/11/1111): "); 
												gets(nascimento); fflush(stdin);
											printf("\n\t\t - Rua: ");
												gets(rua); strupr(rua); fflush(stdin);
											printf("\n\t\t - Número: ");
												gets(numero); fflush(stdin);
											printf("\n\t\t - Bairro: ");
												gets(bairro); strupr(bairro); fflush(stdin);
											printf("\n\t\t - Estado: ");
												gets(estado); strupr(estado); fflush(stdin);
											printf("\n\n--------------------------------------------------------------------------");
											printf("\n\n------------------------------- NOTA FISCAL ------------------------------\n");
											printf("\n Nome  ");
												printf("\n  %s", nome);
											printf("\n CPF ");
												printf("\n  %s", cpf);
											printf("\n Data de nascimento");
												printf("\n  %s", nascimento);
											printf("\n\n Endereço ");
											printf("\n  %s   %s    %s    %s", rua, numero, bairro, estado);
											printf("\n\n Produto \t\t\t Quantidade \t\t Valor Total");
											total=qtdSuvinil * 73 ;
											printf("\n  Tinta Suvinil Azul 3,6L \t %d \t\t\t %.2f", qtdSuvinil, total);
											printf("\n\n--------------------------------------------------------------------------");
											printf("\n\n--------------------------------------------------------------------------");
											
											printf("\n\t O prazo para entrega é 5 dias úteis. \n\t Não esqueça de deixar alguém em casa! \n\t Obrigado pela compra. \n\n\n");
										}

						}
						else if(codigo==2)
								{
									printf("\n\t\tTinta Coral Branco 3,6L \n\t\t Digite a quantidade desejada: ");
										scanf("%d", &qtdCoral);
									printf("\n\tQuantidade escolhida: %d", qtdCoral);
									
									fflush(stdin);
									printf("\n\t Próximo passo: \n\t\t [1] Excluir produto \n\t\t [2] Continuar");
									printf("\n\t\tEscolha: ");
										scanf("%d", &continuar);
										if (continuar ==1)
										{
											printf("\n\t Ok, estou excluindo seus produtos do carrinho...");
											printf("\n\n\t Vou abrir o catálogo para você escolher novamente. \n\n");
											venda ();		
										}
										
										else if (continuar ==2)
											{
												fflush(stdin);
												printf("\n\n\t Agora vamos agilizar as coisas para a sua entrega! ");
												printf("\n\tInforme \n\t\t - Nome: ");
													gets(nome); strupr(nome); fflush(stdin);
												printf("\n\t\t - CPF(Somente números): "); 
													gets(cpf); fflush(stdin);
												printf("\n\t\t - Data de nascimento (11/11/1111): "); 
													gets(nascimento); fflush(stdin);
												printf("\n\t\t - Rua: ");
													gets(rua); strupr(rua); fflush(stdin);
												printf("\n\t\t - Número: ");
													gets(numero); fflush(stdin);
												printf("\n\t\t - Bairro: ");
													gets(bairro); strupr(bairro); fflush(stdin);
												printf("\n\t\t - Estado: ");
													gets(estado); strupr(estado); fflush(stdin);
												printf("\n\n--------------------------------------------------------------------------");
												printf("\n\n------------------------------- NOTA FISCAL ------------------------------\n");
												printf("\n Nome  ");
													printf("\n  %s", nome);
												printf("\n CPF ");
													printf("\n  %s", cpf);
												printf("\n Data de nascimento");
													printf("\n  %s", nascimento);
												printf("\n\n Endereço ");
												printf("\n  %s   %s    %s    %s", rua, numero, bairro, estado);
												printf("\n\n Produto \t\t\t Quantidade \t\t Valor Total");
												total=qtdCoral * 79 ;
												printf("\n  Tinta Suvinil Azul 3,6L \t %d \t\t\t %.2f", qtdCoral, total);
												printf("\n\n--------------------------------------------------------------------------");
												printf("\n\n--------------------------------------------------------------------------");
												printf("\n\t O prazo para entrega é 5 dias úteis. \n\t Não esqueça de deixar alguém em casa! \n\t Obrigado pela compra. \n\n\n");

										}
									}
										else if(codigo==3)
											{
												printf("\n\t\tTinta Suvinil Preto 3,6L \n\t\t Digite a quantidade desejada: ");
													scanf("%d", &qtdSP);
												printf("\n\tQuantidade escolhida: %d", qtdSP);
												
												fflush(stdin);
												printf("\n\t Próximo passo: \n\t\t [1] Excluir produto \n\t\t [2] Continuar");
												printf("\n\t\tEscolha: ");
													scanf("%d", &continuar);
													if (continuar ==1)
													{
														printf("\n\t Ok, estou excluindo seus produtos do carrinho...");
														printf("\n\n\t Vou abrir o catálogo para você escolher novamente. \n\n");
														venda ();		
													}
													
													else if (continuar ==2)
														{
															fflush(stdin);
															printf("\n\n\t Agora vamos agilizar as coisas para a sua entrega! ");
															printf("\n\tInforme \n\t\t - Nome: ");
																gets(nome); strupr(nome); fflush(stdin);
															printf("\n\t\t - CPF(Somente números): "); 
																gets(cpf); fflush(stdin);
															printf("\n\t\t - Data de nascimento (11/11/1111): "); 
																gets(nascimento); fflush(stdin);
															printf("\n\t\t - Rua: ");
																gets(rua); strupr(rua); fflush(stdin);
															printf("\n\t\t - Número: ");
																gets(numero); fflush(stdin);
															printf("\n\t\t - Bairro: ");
																gets(bairro); strupr(bairro); fflush(stdin);
															printf("\n\t\t - Estado: ");
																gets(estado); strupr(estado); fflush(stdin);
															printf("\n\n--------------------------------------------------------------------------");
															printf("\n\n------------------------------- NOTA FISCAL ------------------------------\n");
															printf("\n Nome  ");
																printf("\n  %s", nome);
															printf("\n CPF ");
																printf("\n  %s", cpf);
															printf("\n Data de nascimento");
																printf("\n  %s", nascimento);
															printf("\n\n Endereço ");
															printf("\n  %s   %s    %s    %s", rua, numero, bairro, estado);
															printf("\n\n Produto \t\t\t Quantidade \t\t Valor Total");
															total=qtdSP * 74.90 ;
															printf("\n  Tinta Suvinil Preto 3,6L \t %d \t\t\t %.2f", qtdSP, total);
															printf("\n\n--------------------------------------------------------------------------");
															printf("\n\n--------------------------------------------------------------------------");
															printf("\n\t O prazo para entrega é 5 dias úteis. \n\t Não esqueça de deixar alguém em casa! \n\t Obrigado pela compra. \n\n\n");
			
														}
											}
			

}
