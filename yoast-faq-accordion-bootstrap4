<?php
function wporg_block_wrapper( $block_content, $block ) {
	if ( $block['blockName'] === 'yoast/faq-block' ) {
		$content = '<div class="schema-faq wp-block-yoast-faq-block">';
		foreach($block['attrs']['questions'] as $question){
			$content .='<div id="faq-question-'.$question['id'].'" class="schema-faq-section">';
			$content .='<a class="schema-faq-question collapsed" role="button" data-toggle="collapse" href="#'.$question['id'].'" aria-expanded="true">'.$question['jsonQuestion'].'</a>';
			$content .='<p class="collapse schema-faq-answer" role="tabpanel" id="'.$question['id'].'">'.$question['jsonAnswer'].'</p>';
			$content .='</div>';
		}
		$content .='</div>';
    return $content;
    }
    return $block_content;
}
 
add_filter( 'render_block', 'wporg_block_wrapper', 10, 2 );
